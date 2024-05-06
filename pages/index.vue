<template>
  <div class="intro-container">
    <div class="animated-background">
      <div class="title-box">
        <div class="align-box">
          <p class="animate__animated animate__fadeIn">W</p>
          <p class="animate__animated animate__fadeIn">J</p>
        </div>
        <div class="align-box">
          <p class="animate__animated animate__fadeIn">P</p>
          <p class="animate__animated animate__fadeIn">O</p>
          <p class="animate__animated animate__fadeIn">R</p>
          <p class="animate__animated animate__fadeIn">T</p>
          <p class="animate__animated animate__fadeIn">F</p>
          <p class="animate__animated animate__fadeIn">O</p>
          <p class="animate__animated animate__fadeIn">L</p>
          <p class="animate__animated animate__fadeIn">I</p>
          <p class="animate__animated animate__fadeIn">O</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  mounted() {
    // setTimeout(() => {
    //   $nuxt.$router.push('/main')
    // }, 2000)
  },
}
</script>

<style lang="scss">
div.intro-container {
  width: 100vw;
  height: 100vh;
  background-color: #bababa;
  position: relative;
  overflow: hidden;
}
div.animated-background {
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: black;
  left: -100%;
  animation: slideIn 2s forwards;
  div.title-box {
    margin: 10px 0 0 10px;
    div.align-box {
      display: flex;
      p {
        margin-right: 4px;
        font-size: 2rem;
        font-weight: bold;
        animation-delay: 2s; // 기본 지연 시간 설정
        &:nth-child(1) {
          animation-delay: 2s;
        }
        &:nth-child(2) {
          animation-delay: 2.1s;
        }
        &:nth-child(3) {
          animation-delay: 2.2s;
        }
        &:nth-child(4) {
          animation-delay: 2.3s;
        }
        &:nth-child(5) {
          animation-delay: 2.4s;
        }
        &:nth-child(6) {
          animation-delay: 2.5s;
        }
        &:nth-child(7) {
          animation-delay: 2.6s;
        }
        &:nth-child(8) {
          animation-delay: 2.7s;
        }
        &:nth-child(9) {
          animation-delay: 2.8s;
        }
      }
    }
  }
  p {
    color: white;
  }
}

@keyframes slideIn {
  from {
    left: -100%; /* 시작 위치 */
  }
  to {
    left: 0; /* 최종 위치 */
  }
}
</style>
