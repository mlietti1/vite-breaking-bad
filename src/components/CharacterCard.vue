<script>
export default {
  name: 'CharacterCard',
  props: {
    character: Object
  }
}
</script>

<template>

  <div class="mc-card p-3">
    <img :src="character.img" :alt="character.name">
    <div>
      <h5>{{character.name}}</h5>
      <p>{{character.category}}</p>
      <p>{{character.status}}</p>
    </div>
  </div>
  
</template>

<style lang="scss" scoped>

@use '../styles/partials/vars' as *;

.mc-card{
  background-color: $primary-color;
  margin: 10px;
  width: calc(100% / 5 - 20px);
  text-align: center;
  img{
    width: 100%;
    margin-bottom: 20px;
  }
  h5{
    color: white;
    text-transform: uppercase;
    margin-bottom: 16px;
  }
  p{
    color: gray;
  }
}


</style>