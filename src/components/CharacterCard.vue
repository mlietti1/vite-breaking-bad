<script>
export default {
  name: 'CharacterCard',
  props: {
    character: Object
  }
}
</script>

<template>

  <div>
    <img src="" alt="">
    <div>
      <h3>{{character.name}}</h3>
      <p>{{character.category}}</p>
      <p>{{character.status}}</p>
    </div>
  </div>
  
</template>

<style lang="scss" scoped>

</style>