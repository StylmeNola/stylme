<template>
  <footer class="footer">
    <div class="container text-center">
      <copywrite />
    </div>
  </footer>
</template>
<script>
import Copywrite from '~/components/Copywrite.vue'
export default {
  components: {
    Copywrite
  }
}
</script>
<style lang="scss" scoped>
  footer {
    margin-top:5rem;
  }
  .container {
    padding: 1.5rem 0;
    border-top: 1px solid #e2e2e2;
  }
</style>
