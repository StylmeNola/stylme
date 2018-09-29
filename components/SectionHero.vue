<template>
  <section class="hero">
    <div class="container pos-r">
      <nav-stylme />
    </div>
  </section>
</template>
<script>
import NavStylme from '~/components/NavStylme.vue'
export default {
  components: {
    NavStylme
  }
}
</script>
<style lang="scss" >
  .hero {
    background: #fff url('~assets/images/hero-bg.jpg') no-repeat center;
    background-size: cover;
    height: 60vh;
    min-height:400px;
    .container {
      max-width:1600px;
    }
  }
</style>
