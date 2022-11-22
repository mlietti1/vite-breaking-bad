<script>

import axios from 'axios';
import {store} from './data/store';

import AppHeader from './components/AppHeader.vue';
import AppSelect from './components/AppSelect.vue';
import CharacterList from './components/CharacterList.vue';


export default {
  name: 'App',
  data(){
    return{
      store
    }
  },
  components: {
    AppHeader,
    AppSelect,
    CharacterList
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
    <AppSelect @selectCategory="getCharacters()" />
    <CharacterList />
  </main>
</template>

<style lang="scss">
@use './styles/general';
</style>