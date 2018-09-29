<template>
  <div class="nav-wrap pos-a full-width">
    <a href="/"><logo /></a>
  </div>
</template>
<script>
import Logo from '~/components/Logo.vue'
export default {
  components: {
    Logo,
  }
}
</script>
<style lang="scss" scoped>
 .nav-wrap {
   left:0;
   top:0;
   padding:1.5rem 0;
 }
</style>
