<template>
    <div class="container">
      <h1>LOS POKEPUERCOS XD</h1>
      <PokemonSearch 
        :apiUrl="apiUrl" 
        @setPokemonUrl="setPokemonUrl" />
      <PokemonList 
        :imageUrl="imageUrl" 
        :apiUrl="apiUrl"
        @setPokemonUrl="setPokemonUrl" />
      <PokemonDetail 
        v-if="showDetail"
        :pokemonUrl="pokemonUrl"
        :imageUrl="imageUrl"
        @closeDetail="closeDetail" />
    </div>
</template>
  
  <script>
    import PokemonSearch from './PokemonSearch.vue';
    import PokemonList from './PokemonList.vue';
    import PokemonDetail from './PokemonDetail.vue';
  
    export default {
      data: () => {
        return {
          imageUrl: 'https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/official-artwork/',
          apiUrl: 'https://pokeapi.co/api/v2/pokemon/',
          pokemonUrl: '',
          showDetail: false
        }
      },
      components: {
        PokemonSearch,
        PokemonList,
        PokemonDetail
      },
      methods: {
        setPokemonUrl(url) {
          this.pokemonUrl = url;
          this.showDetail = true;
        },
        closeDetail() {
          this.pokemonUrl = '';
          this.showDetail = false;
        }
      }
    }
  </script>
  
  <style>
  /*@import url('https://fonts.googleapis.com/css?family=Acme');*/
   .container {
    
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    padding: 10px;
    width: calc(100% - 20px);
    min-height: calc(100vh - 20px);
    background: radial-gradient(#c30a0a, #0A2E50);

    font-family: 'Acme', arial;
    font-size: 1rem;
    font-weight: normal;
  }
  h1 {
      font-family:'Courier New', Courier, monospace;
    font-size: 50px;
    color: rgb(236, 189, 23);
  }
  </style>
  