<template>
  <div class="sidebar-container">
    <div class="animate__animated animate__fadeIn animate__delay-3s side-bar">
      <div class="img-box">
        <img src="/icons/menu.png" alt="menu" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SidebarComponent',
}
</script>

<style lang="scss">
@import '~/assets/common.scss';

div.sidebar-container {
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
}
</style>
