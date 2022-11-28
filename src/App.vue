<template>
   <div id="app">
    <PokemonPoke />
  </div>
</template>

<script>
import PokemonPoke from './components/PokemonPoke.vue';

export default {
  components: {
    PokemonPoke
  }
}
</script>

<style>
body {
    margin: 0;
    padding: 0;
    
    background-image: url('https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.gratistodo.com%2Fpokemon-wallpapers%2F&psig=AOvVaw2_uTFAhO9J4uin7yVDPVIE&ust=1669693272315000&source=images&cd=vfe&ved=0CA0QjRxqFwoTCJiKy6b6z_sCFQAAAAAdAAAAABAD');
   
  }
</style>
