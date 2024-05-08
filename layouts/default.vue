<template>
  <div class="layout-container">
    <Nuxt />
    <SideBarComponent />
    <div id="cursor-dot"></div>
  </div>
</template>

<script>
import { gsap } from 'gsap'

export default {
  name: 'BasicLayout',
  mounted() {
    const cursor = document.getElementById('cursor-dot')
    document.addEventListener('mousemove', (e) => {
      gsap.to(cursor, {
        x: e.clientX,
        y: e.clientY,
        duration: 0.2,
        ease: 'Power1.easeOut',
      })
    })
  },
}
</script>

<style lang="scss">
@import '~/assets/common.scss';

div.layout-container {
  position: relative;
  #cursor-dot {
    position: fixed;
    width: 10px;
    height: 10px;
    background-color: #ffffff;
    border-radius: 50%;
    pointer-events: none;
    transform: translateX(-50%) translateY(-50%);
    z-index: 9999;
    top: 0;
    left: 0;
  }
}
</style>
