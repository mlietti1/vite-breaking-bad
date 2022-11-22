<script>

import { store } from '../data/store';

export default {
  name: 'AppSelect',
  data(){
    return{
      store
    }
  }
}
</script>

<template>
  <div class="container">
    <div class="row mb-4">
      <div class="col-auto">
        <select v-model="store.categoryToSelect" class="form-select" aria-label="Default select example">
          <option value="" selected>Select Category</option>
          <option value="Breaking Bad">Breaking Bad</option>
          <option value="Better Call Saul">Better Call Saul</option>
        </select>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>

</style>