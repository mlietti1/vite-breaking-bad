<script>

import axios from 'axios';
import {store} from './data/store';

import AppHeader from './components/AppHeader.vue';
import AppSearch from './components/AppSearch.vue';
import CharacterList from './components/CharacterList.vue';
import ResultCharacters from './components/ResultCharacters.vue';

export default {
  name: 'App',
  data(){
    return{
      store
    }
  },
  components: {
    AppHeader,
    AppSearch,
    CharacterList,
    ResultCharacters
  },
  methods:{
    getCharacters(){
      store.isLoaded = false
      axios.get(store.apiUrl, {
        params:{
          category: store.categoryToSelect
        }
      })
        .then(result => {
          store.charactersListData = result.data;
          store.isLoaded = true;
        })
        .catch (error => {
          console.log(error);
        })
        }
  },
  mounted(){
    this.getCharacters()
  }
}
</script>

<template>
  <AppHeader title="Breaking Bad Api" />
  <main>
    <AppSearch @selectCategory="getCharacters()" />
    <ResultCharacters />
    <CharacterList />
  </main>
</template>

<style lang="scss">
@use './styles/general';
</style>