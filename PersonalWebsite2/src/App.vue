<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HomeView from './views/HomeView.vue';
import AboutView from './views/AboutView.vue';
import PortfolioView from './views/PortfolioView.vue';
import ContactView from './views/ContactView.vue';
import { ref, onMounted, onBeforeUnmount, computed } from 'vue';

const scrollPosition = ref(0)
const handleScroll = () => {
  scrollPosition.value = window.scrollY;
};
onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})
onBeforeUnmount(() => {
  window.addEventListener('scroll', handleScroll)
})
const hamColor = computed(() => {
      if (scrollPosition.value < 620) {
        return 'black';
      } else {
        return 'white';
      }
});

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
  <HomeView id="home"></HomeView>
  <AboutView id="about"></AboutView>
  <PortfolioView id="portfolio"></PortfolioView>
  <ContactView id="contact"></ContactView>

  <svg @click="handleHamburger" :ham-color=[hamColor] class="hamburger" viewBox="0 0 60 60" :hamburger-toggle=[hamburgerToggle]>
    <rect class="top" ></rect>
    <rect class="middle" ></rect>
    <rect class="bottom" ></rect>
    <rect class="x-1"></rect>
    <rect class="x-2"></rect>
  </svg>
  <main-background>
    <nav>
      <router-link @click="handleHamburger" class="link" :to="{hash: '#home'}">Home</router-link>
      <router-link @click="handleHamburger" class="link" :to="{hash: '#about'}">About</router-link>
        <router-link @click="handleHamburger" class="link" :to="{hash: '#portfolio'}">Portfolio</router-link>
        <router-link @click="handleHamburger" class="link" :to="{hash: '#contact'}">Contact</router-link>
  </nav>

  </main-background>
</template>

<style scoped>
.hamburger[ham-color="white"]{
  fill:white;
}
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
  height: 0%;
  width: 0%;
  position: fixed;
  background-color: var(--main-yellow);
  top: 0; 
  right: 0;
  transition: width 1s ease,height 0s ease-in 1s, background-color 2s ease;
  display: flex;
  flex-direction: column;
  align-items: start;
  justify-content: space-evenly;

}
main-background nav .link{
  font-size:0px;
  color:white;
  text-decoration: none;
  margin: 0 auto;
  transition:all 0s ease;
}
.hamburger[hamburger-toggle="true"] + main-background nav .link{
  font-size:25px;
  transition:all .1s ease 1.1s;
}
main-background{
  width: 0;
  height: 100%;
  background-color: var(--main-orange);
  position: fixed;
  right:0;
  top: 0;
  transition:  width 1s ease, background-color 2s ease;
  z-index: 9;
}
.hamburger[hamburger-toggle="true"] + main-background nav{
  background-color: var(--main-orange);
  width: 20rem;
  height:100%;
  z-index: 9;
  transition: width .5s ease, height .5s ease-in .5s, background-color 4s ease .5s;
}
.hamburger[hamburger-toggle="true"] + main-background{
  width:100%;
  height: 100%;
  background-color: rgb(255, 210, 63,.9);
  transition: width 1s ease, background-color 4s ease;
  z-index: 9;
}
@media (min-width: 1024px) {
  
}
@media (max-width: 1023px) and (min-width:480px){

}
@media (max-width: 480px){
  
}

</style>
