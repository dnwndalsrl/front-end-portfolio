<template>
  <div class="layout-container">
    <Nuxt />
    <div class="animate__animated animate__fadeIn animate__delay-3s side-bar">
      <div class="img-box">
        <img src="/icons/menu.png" alt="menu" />
      </div>
    </div>
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
  div.side-bar {
    display: flex;
    align-items: center;
    justify-content: center;
    position: fixed;
    width: 100px;
    height: 100vh;
    background-color: #bababa;
    top: 0;
    right: 0;
    @include break-sp-sm {
      width: 100%;
      height: 4rem;
      justify-content: end;
    }
    @include break-mc {
      width: 100%;
      height: 4rem;
      justify-content: end;
    }
    div.img-box {
      width: 3rem;
      cursor: pointer;
      -webkit-tap-highlight-color: transparent !important;
      transform: rotate(90deg);
      @include break-sp-sm {
        width: 2rem;
        transform: rotate(180deg);
        margin-right: 0.8rem;
      }
      @include break-mc {
        width: 2rem;
        transform: rotate(180deg);
        margin-right: 0.8rem;
      }
    }
  }
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
