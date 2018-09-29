<template>
  <section class="section-3">
    <div class="container">
      <a class="card flex " v-on:click="$emit('book-link')">
        <div class="img-wrap pos-r overflow-hidden">
          <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" alt="Bridal" class="full-width">
        </div>
        <div class="text-wrap white flex">
         <div class="inner-text pos-r">
            <div class="icon white dib"></div>
            <h3 class="card-title bold">Bridal</h3>
            <p class="card-text">Lorem ipsum dolor sit amet, consectetur adipi elit. In sed purus sit am.</p>
            <p class="card-text-sm">Lorem ipsum dolor sit  amet, consectetur adipi orem ipsum dolor sit  amet      consectetur adipi orem ipsum dolor sit  amet, consectetur </p>
            <a class="link bold db">Book Now</a>
         </div>
        </div>
      </a>
    </div>
  </section>
</template>
<script>
export default {

}
</script>
<style lang="scss" scoped>
  section {
    padding:3rem 0;
  }
  .img-wrap {
    flex: 1 1 50%;
    background-image: url(~assets/images/img-4.jpg);
  }
  .text-wrap {
    text-align: center;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    flex:1 1 50%;
    padding:2rem 2.5rem;
  }
  .inner-text {
    max-width:90%;
  }
  .card-text-sm {
    padding: 2rem 3rem;
    font-size: 20px;
    line-height: 1.3;
    color:$grey;
  }
  .icon {
    background-image: url(~assets/images/dry-icon.png);
    top: -65px;
  }
  .link {
    padding:0 25px 25px;
  }
  @media screen and (min-width:993px){
    .text-wrap {min-height:600px;}
  }
  @media screen and (max-width:992px){
    section {padding-top:0;}
    .img-wrap {flex:1 1 45%}
    .text-wrap {flex:1 1 55%;}
    .card-title {font-size: 22px;}
    .card-text {font-size:20px}
    .card-text-sm {font-size:16px;padding: 25px 0rem;}
    .link {font-size: 22px;}
  }
  @media screen and (max-width:659px){
    .card {
      flex-direction: column;
    }
    .icon {position: absolute;}
    .img-wrap{max-height: 440px;}
  }
</style>
