<script>
import {store} from '../data/store'
export default {
  name: 'ResutlCharacters',
  data(){
    return{
      store
    }
  }
}
</script>

<template>
  <div class="container">
    <p>Characters found: {{store.charactersListData.length}}</p>
  </div>
</template>

<style lang="scss" scoped>

p {
  color: white;
}

</style>