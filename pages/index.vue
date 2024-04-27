<template>
  <div class="intro-container">
    <p>인트로중...</p>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  mounted() {
    setTimeout(() => {
      $nuxt.$router.push('/main')
    }, 2000)
  },
}
</script>

<style lang="scss">
div.intro-container {
  p {
    color: red;
  }
}
</style>
