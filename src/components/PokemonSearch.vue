<template>
    <div class="searchbar">
      <form @submit.prevent="setPokemonUrl">
        <input type="text" v-model="searchvalue">
      </form>
      <i class="fas fa-search" @click="setPokemonUrl"></i>
    </div>
  </template>
  
  <script>
    export default {
      name: 'PokemonSearch',
      props: [
        'apiUrl'
      ],
      data: () => {
        return {
          searchvalue: '',
        }
      },
      methods: {
        setPokemonUrl(url) {
          if(this.searchvalue !== '')
            this.$emit('setPokemonUrl', this.apiUrl + this.searchvalue);
            console.log(url);
        }
      }
    }
  </script>
  
  <style>
    body{
    background-image: url('https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.gratistodo.com%2Fpokemon-wallpapers%2F&psig=AOvVaw2_uTFAhO9J4uin7yVDPVIE&ust=1669693272315000&source=images&cd=vfe&ved=0CA0QjRxqFwoTCJiKy6b6z_sCFQAAAAAdAAAAABAD');
  } 
  .searchbar {
    position: relative;
    width: 100%;
    max-width: 510px;
    padding-bottom: 20px;    
  }

  input {
      border: none;
      outline: none;
      border-radius: 5px;
      padding: 10px 40px 10px 10px;
      width: calc(100% - 50px);
      font-size: 1rem;
      box-shadow: 0 15px 30px rgba(0,0,0,.2),
                  0 10px 10px rgba(0,0,0,.2);
    }

  i {
      position: absolute;
      top: 10px;
      right: 10px;
      font-size: 1.25rem;
      color: #0A2E50;
      cursor: pointer;
    }

  </style>
  