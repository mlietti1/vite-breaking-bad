<script>
export default {
  name: 'AppLoading',
  props:{
    title: String
  }
}
</script>

<template>
  <div class="loader-container d-flex align-items-center justify-content-center flex-column">
    <p>{{title}}</p>
    <div class="lds-ripple"><div></div><div></div></div>

  </div>
</template>

<style lang="scss" scoped>

@use '../styles/partials/vars' as *;

.loader-container {
  height: 500px;
  p{
    color: $primary-color;
  }
}
  .lds-ripple {
  display: inline-block;
  position: relative;
  width: 80px;
  height: 80px;
}
.lds-ripple div {
  position: absolute;
  border: 4px solid $primary-color;
  opacity: 1;
  border-radius: 50%;
  animation: lds-ripple 1s cubic-bezier(0, 0.2, 0.8, 1) infinite;
}
.lds-ripple div:nth-child(2) {
  animation-delay: -0.5s;
}
@keyframes lds-ripple {
  0% {
    top: 36px;
    left: 36px;
    width: 0;
    height: 0;
    opacity: 0;
  }
  4.9% {
    top: 36px;
    left: 36px;
    width: 0;
    height: 0;
    opacity: 0;
  }
  5% {
    top: 36px;
    left: 36px;
    width: 0;
    height: 0;
    opacity: 1;
  }
  100% {
    top: 0px;
    left: 0px;
    width: 72px;
    height: 72px;
    opacity: 0;
  }
}

</style>