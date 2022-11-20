<script>
export default {
  name: 'AppHeader',
  props:{
    title: String
  }
}
</script>

<template>
  <div class="d-flex p-3">
    <img src="/Breaking_Bad_logo.svg" alt="logo">
    <h1>{{title}}</h1>
  </div>
</template>

<style lang="scss" scoped>

img {
  height: 40px;
  margin-right: 1rem;
}
h1 {
  font-weight: 700;
}

</style>