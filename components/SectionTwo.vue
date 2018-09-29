<template>
  <section class="section-2">
    <div class="container">
      <div class="card-wrap flex pos-r">
        <a  class="card flex white text-center" 
          v-for="(card, i) in cards" 
          :key="`card-[${i}]`"
          v-on:click="$emit('book-link')">
          <div class="content flex full-width">
            <div class="img-wrap pos-r overflow-hidden" :style="{backgroundImage: `url(${card.image})`}">
              <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" :alt="card.title" class="full-width">
            </div>
            <div class="text-wrap pos-r white dib">
              <div class="icon white pos-a" :style="{backgroundImage: `url(${card.icon})` }">
              </div>
              <h3 class="card-title bold">{{card.name}}</h3>
              <p class="card-text">{{card.content}}</p>
              <a  class="link hide-on-medium-and-up">Book Now</a>
            </div>
          </div>
        </a>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data()  {
    return {
      cards: [
        {
          name: 'Blowout',
          content: 'Lorem ipsum dolor sit amet, consectetur adipi elit. In sed purus sit am onsectetur adipi elit. In sed purus sit am',
          image: require('~/assets/images/img-1.jpg'),
          icon: require('~/assets/images/dry-icon.png'),
        },
        {
          name: 'Makeup',
          content: 'Lorem ipsum dolor sit amet, consectetur adipi elit. In sed purus sit am',
          image: require('~/assets/images/img-2.jpg'),
          icon: require('~/assets/images/makeup-icon.png'),
        },
        {
          name: 'Styling',
          content: 'Lorem ipsum dolor sit amet, consectetur adipi elit. In sed purus sit am',
          image: require('~/assets/images/img-3.jpg'),
          icon: require('~/assets/images/scissor-icon.png'),
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  section { 
    padding:3rem 0
  }
  .card-wrap {
    justify-content: space-between;
  } 
  .card {
    width: 33.3333%;
    &:nth-child(2){
      margin:0 3.5%;
    }
  }
  .content {
    flex-direction: column;
  }
  .img-wrap{
    max-height: 440px;
  }
  .text-wrap {
    flex:1 0 auto;
    padding:2rem 2.5rem;
  }
  
  @media screen and (max-width:1200px){
    .card-title,
    .link {
        font-size:22px
      }
    .card-text {
      font-size:20px
    }
  }
  @media screen and (max-width:992px){
    .card-wrap{
      display:block
    }
    .card{width:100%;
      &:nth-child(2){
        margin:3rem 0;
      }
    }
    .text-wrap .link{
      display:block;
    }
  } 
  @media screen and (max-width:992px) and (min-width:660px){
    .content{
      flex-direction:row;
    }
    .img-wrap {
      flex: 1 1 45%;
    }
    .text-wrap{
      display: flex;
      flex-direction: column;
      justify-content: center;
      flex:1 1 55%;
    }
    .icon {
      position: relative;
      top:0;
    }
  }
</style>
