<template>
  <div>
    <section-hero />
    <section-one />
    <section-two v-on:book-link="modalToggle" key="1" />
    <section-three v-on:book-link="modalToggle" key="2" /> 
    <section-footer />
    <transition name="modal" mode="out-in">
      <aside class="modal" v-show="modal">
        <div class="modal-content">
          <button class="close" @click="modalToggle">X</button> 
          <iframe src="https://app.acuityscheduling.com/schedule.php?owner=16684796" width="100%" height="800" frameBorder="0"></iframe>
         </div>
      </aside>
    </transition>
    
  </div>
</template>

<script>

import SectionHero from '~/components/SectionHero.vue'
import SectionOne from '~/components/SectionOne.vue'
import SectionTwo from '~/components/SectionTwo.vue'
import SectionThree from '~/components/SectionThree.vue'
import SectionFooter from '~/components/SectionFooter.vue'

export default {
  head(){
    return {
      script: [
        {src: 'https://d3gxy7nm8y4yjr.cloudfront.net/js/embed.js'}
      ]
    }
  },
  components: {
    SectionHero,
    SectionOne,
    SectionTwo,
    SectionThree,
    SectionFooter
  },
  data() {
    return {
      modal: false
    }
  },
  methods: {
    modalToggle: function(){
      this.modal = !this.modal
      document.body.classList.toggle('overflow-hidden')
    }
  }
}
</script>
<style lang="scss" >
  body {
    background:#f5f4f5;
  }
    // cards
  .card-title {
    color:$grey;
    font-size: 30px;
    padding:.5rem 0 1rem;
  }
  .card-text {
    font-size:30px;
    font-weight: 100;
    color:black;
  }
  .link {
    color:$grey-dark;
    font-size:24px;
    padding:25px;
    font-weight: 100;
  }
  .icon {
    background-size:80%;
    background-position: center;
    width:70px;
    height:70px;
    left:calc(50% - 35px);
    padding:10px;
    border-radius: 50%;
    top: -30px;
  } 

  .card {
    box-shadow: 0px 2px 20px -3px rgba(0, 0, 0, 0.21176470588235294);
    .img-wrap{
      background-size:cover;
      background-position: center;
      background-repeat: no-repeat;
      &:before,
      &:after {
        position: absolute;
        left: 0;
        opacity: 0;
      }
    &:before{
      content: '';
      width: 0;
      height: 0;
      background: rgba(255, 255, 255, 0.5803921568627451);
      top: 0;  
      transition: .3s ease;
    }
    &:after {
      content: "Book Now";
      text-align: center;
      font-size: 33px;
      height: 100%;
      width:100%;
      top: 55%;
      left: 0;
      color: #fff;
      text-shadow: 1px 1px 1px black;
      font-weight: bold;
      transition: opacity 0s ease;
      transition-delay:0s;
    }
  }
  &:hover {
    .img-wrap {
      &:before {
        width: 100%;
        height: 100%;
        opacity: 1;
      }
      &:after {
        opacity: 1;
        top: 50%;
        opacity: 1;
        transition: .5s ease;
        transition-delay:.2s;
      }
    }
  }
}
.modal {
  position: fixed;
  z-index: 1; 
  left: 0;
  top: 0;
  width: 100%; 
  height: 100%; 
  overflow: auto; 
  background-color: rgba(239, 239, 239, 0.9);
  transition: opacity .3s ease;
  .modal-content {
    max-width: 900px;
    padding:0 15px;
    margin:3% auto;
    text-align: right;
    
    transition: all .3s ease;
    .close {
      font-size: 18px;
      border-radius: 50%;
      line-height: 45px;
      display: inline-block;
      width: 50px;
    }
  }
}
.modal-enter {opacity: 0;}
.modal-leave-active {opacity: 0;}
.modal-enter .modal-content,
.modal-leave-active .modal-content {-webkit-transform: scale(1.1);transform: scale(1.1);
}
</style>

