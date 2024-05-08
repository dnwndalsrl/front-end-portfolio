<template>
  <div class="layout-container">
    <Nuxt />
    <div
      class="animate__animated animate__fadeIn animate__delay-3s side-bar"
    ></div>
  </div>
</template>

<script>
export default {
  name: 'BasicLayout',
}
</script>

<style lang="scss">
@import '~/assets/common.scss';

div.layout-container {
  position: relative;
  div.side-bar {
    position: fixed;
    width: 100px;
    height: 100vh;
    background-color: #bababa;
    top: 0;
    right: 0;
    @include break-sp-sm {
      width: 100%;
      height: 4rem;
    }
    @include break-mc {
      width: 100%;
      height: 4rem;
    }
  }
}
</style>
