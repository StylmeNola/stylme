<template>
  <section class="section-1 text-center flex">
    <div class="container">
      <h2>Beauty on Demand</h2>
      <p>Stylme is a mobile On-demand beauty service offering blowouts, makeup and mens cuts. 
  We come to individuals and groups for everyday, photoshoots, weddings, bachelorette 
  parties, girls night and beyond. We love working with women/men and  all hair types! </p>
    </div>
  </section>
</template>
<style lang="scss" scoped>
  section{
    color: $grey-dark;
    font-size: 30px;
    min-height: 35vh;
    align-items: center;
    padding: 3rem 0;
  }
  h2 {
    font-size:48px;
    padding-bottom: 2rem;
  }
  p {
    line-height:1.3;
    max-width:1200px;
    margin:0 auto;
  }
  @media screen and (max-width:1200px){
    section{padding:3rem 0 1rem}
    h2{font-size:36px}
    p{font-size:24px;}
  }
</style>
