<script>
import {store} from '../data/store'
export default {
  name: 'ResutlCharacters',
  data(){
    return{
      store
    }
  },
  computed: {
    resultString(){
      return 'Characters found: ' + store.charactersListData.length;
    }
  }
}
</script>

<template>
  <div class="container">
    <p>{{resultString}}</p>
  </div>
</template>

<style lang="scss" scoped>

p {
  color: white;
}

</style>