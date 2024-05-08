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
      <div
        class="sub-title-box animate__animated animate__fadeIn animate__delay-3s"
      >
        <div class="line"></div>
        <p>portfolio</p>
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
@import '~/assets/common.scss';

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
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  div.title-box {
    margin: 5rem 0 0 0.5rem;
    @include break-sp-sm {
      margin: 8rem 0 0 0.5rem;
    }
    @include break-mc {
      margin: 10rem 0 0 0.5rem;
    }
    div.align-box {
      display: flex;
      p {
        font-size: 7rem;
        margin-right: 4px;
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
        @include break-sm {
          font-size: 6rem;
        }
        @include break-sp-sm {
          font-size: 5rem;
        }
        @include break-mc {
          font-size: 3.5rem;
        }
      }
    }
  }
  div.sub-title-box {
    margin-bottom: 30px;
    div.line {
      height: 1px;
      width: 80%;
      background-color: #ffffff;
      margin-bottom: 8px;
    }
    p {
      font-size: 1.5rem;
      margin-left: 10px;
      @include break-sm {
        font-size: 1.3rem;
      }
      @include break-sp-sm {
        font-size: 1.3rem;
      }
      @include break-mc {
        font-size: 1.2rem;
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
