<script>
import axios from 'axios';
import AppPokemonMain from './components/AppPokemonMain.vue';
import AppPokemonHeader from './components/AppPokemonHeader.vue';
import {store} from './store'


export default {
  components: {
    AppPokemonMain,
    AppPokemonHeader,
  },
  data() {
    return {
      store
      
    }
  },mounted() {
    axios.get(store.apiUrl).then((response)=> {
      store.pokemonList = response.data.docs
      console.log(store.pokemonList)
    })
    
  },
}
</script>

<template>
  <div>
    <AppPokemonHeader />
    <AppPokemonMain />
  </div>
</template>

<style lang="scss">
  @use './styles/generals.scss' as *;
</style>