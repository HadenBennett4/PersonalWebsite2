<script setup>
import { ref } from 'vue'

const show = ref("false");

function changeShow(){
    if(show.value==="false"){
        show.value = "true";
    }else{
        show.value = "false";
    }
}
</script>

<template>
   <div class="container">
    <div class="wrapper">
        <div :showThis=[show] class="about">
            <div  class="about-header">
            <h1>ABOUT ME</h1>
            <div @click="changeShow()" class="close-open-button">Learn More</div>
        </div>
        <div class="about-info">
            <h1>This is what is about me</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia dolorum, quis nobis itaque id nulla quas inventore impedit aliquam neque voluptates nostrum quos vel sint dicta quae vitae. Nobis, obcaecati!</p>
            <div @click="changeShow()" class="close-open-button">Close</div>
        </div>
        </div>
    </div>
   </div>
</template>

<style scoped>
@media (min-width: 1024px) {
    .container{
        width: 100%;
        height: 800px;
    }
    .wrapper{
        width:100%;
        height: 100%;
        background-color: black;
        display: flex; flex-direction: column;
        align-items: center;
        justify-content: center;
        overflow-x:hidden;
        overflow-y: hidden;
    }
    .about{
        width: 400%;
        height:42%;
        display: grid;
        grid-template-columns: repeat(3,1fr);
        background-image: url(../assets/Back.png);
        transition: all 1.5s ease;
        transform:rotate(-20deg);
        box-shadow: 0 0 0 4px var(--main-yellow),
                    0 0 0 8px var(--main-orange),
                    0 0 0 12px var(--secondary-yellow);

    }
    .about-info,.about-header{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        transition: all 1s ease;
        background-color: rgb(25,25,25);
    }
    .about-info{
        grid-column-start: 3;
        margin-left:-1%;
    }
    .about-header{
        grid-column-start: 2;
    }
    .about[showThis="true"] .about-header{
            transform: translateX(-100%);
    }
    .about[showThis="true"] .about-info{
            transform: translateX(-100%);
    }
    

  
}
@media (max-width: 1023px) and (min-width:480px){

}
@media (max-width: 480px){
  
}
</style>
