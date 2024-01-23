<script setup lang="ts">
import { ref } from 'vue'
import { RouterLink, RouterView } from 'vue-router'
import HomeView from './views/HomeView.vue';
import AboutView from './views/AboutView.vue';
import PortfolioView from './views/PortfolioView.vue';
import ContactView from './views/ContactView.vue';

const hamburgerToggle = ref("false")
function handleHamburger(){
  if(hamburgerToggle.value === "false"){
    hamburgerToggle.value = "true";
  }else{
    hamburgerToggle.value = "false";
  }
  console.log();
}
</script>

<template>
  <HomeView></HomeView>
  <AboutView></AboutView>
  <PortfolioView></PortfolioView>
  <ContactView></ContactView>

  <svg @click="handleHamburger" class="hamburger" viewBox="0 0 60 60" :hamburger-toggle=[hamburgerToggle]>
    <rect class="top" ></rect>
    <rect class="middle" ></rect>
    <rect class="bottom" ></rect>
    <rect class="x-1"></rect>
    <rect class="x-2"></rect>
  </svg>
  <main-background>
    <nav>
    
  </nav>

  </main-background>
</template>

<style scoped>
.hamburger{
  position: fixed;
  top: 0; 
  right: 0;
  width: 60px;
  height: 60px;
  margin-right: 10px;
  margin-top: 10px;
  z-index: 10;
}
.top,.middle,.bottom{
  width:80%;
  height: 5px;
  x:5;
  rx:2px;
  transition: all .5s ease;
}
.top{
  y:14;
}
.middle{
  y:30;
}
.bottom{
  y:46;
}
.x-1,.x-2{
  width: 80%;
  height: 5px;
  rx:2px;
  y:30;
  transition: all .5s ease;
  transform-origin: center;
}
.x-1{
  x:-95;
  rotate:45deg;
}
.x-2{
  x:105;
  rotate:-45deg;
}
.hamburger[hamburger-toggle="true"] .middle{
  x:-50;
  rotate:180deg;
}
.hamburger[hamburger-toggle="true"] .top,.hamburger[hamburger-toggle="true"] .bottom{
  y:30;
  rotate:180deg;
}
.hamburger[hamburger-toggle="true"] .x-1,.hamburger[hamburger-toggle="true"] .x-2{
  x:6;
}

/**Styles for the nav bar */
main-background nav{
  height: 0rem;
  width: 20rem;
  position: fixed;
  background-color: var(--main-yellow);
  top: 0; 
  right: 0;
  transition: height 1.5s ease-in, background-color 2s ease;
}
main-background{
  width: 0;
  height: 100%;
  background-color: var(--main-orange);
  position: fixed;
  right:0;
  top: 0;
  transition:  width 1s ease, background-color 2s ease;
}
.hamburger[hamburger-toggle="true"] + main-background nav{
  background-color: var(--main-orange);
  width: 20rem;
  height:100rem;

  transition: height 2s ease-in .5s, background-color 4s ease 1s;
}
.hamburger[hamburger-toggle="true"] + main-background{
  width:100%;
  height: 100%;
  background-color: rgb(255, 210, 63,.9);
  transition: width 2s ease, background-color 4s ease;
}
@media (min-width: 1024px) {
  
}
@media (max-width: 1023px) and (min-width:480px){

}
@media (max-width: 480px){
  
}

</style>
