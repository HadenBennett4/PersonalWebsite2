<template>
  <home>
    <img src="../assets/Dallas.jpeg" alt="" class="home-image">
    <h1>HADEN BENNETT</h1>
    <scroll-down-button>
      
    </scroll-down-button>
  </home>
</template>

<style scoped>
home{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 600px;
}
.home-image{
  width: 100%;
  filter:grayscale(60%);
  object-fit: fill;
  position: absolute;
  z-index:-2;
}
h1{
  font-size: 120px;
  font-weight: bolder;
  color: var(--main-white);
  text-shadow:2px 2px 0 var(--secondary-yellow),
  4px 4px 0 var(--main-orange),
  6px 6px 0 var(--main-yellow);
}
@media (min-width: 1024px) {
  
}
@media (max-width: 1023px) and (min-width:480px){

}
@media (max-width: 480px){
  
}
</style>
