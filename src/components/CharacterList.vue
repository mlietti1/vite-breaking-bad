<script>

import {store} from '../data/store';
import CharacterCard from './CharacterCard.vue';
import AppLoading from './AppLoading.vue';

export default {
  name: 'CharacterList',
  components:{
    CharacterCard,
    AppLoading
  },
  data(){
    return {
      store
    }
  }
}
</script>

<template>
  <div class="container">
    <div v-if="store.isLoaded" class="d-flex flex-wrap">
      <CharacterCard v-for="character in store.charactersListData" :key="character.char_id" :character="character" />
    </div>
    <div v-else>
      <AppLoading title="Loading..." />
    </div>
  </div>
</template>

<style lang="scss" scoped>

.container {
  background-color: white;
  padding: 2rem 1rem;
}

</style>