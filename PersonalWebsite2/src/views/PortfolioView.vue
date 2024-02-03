<script setup>
import { ref } from 'vue'
import ProjectModal from '../components/ProjectModal.vue'

const showModal = ref(0);
function changeModal(num){
    if(showModal.value === num){
        showModal.value = 0;
    }else{
    showModal.value = num;
    }

}
</script>

<template>
    <div class="container">
        <h1>My Portfolio</h1>
        <div :show-modal=[showModal] class="grid">
            <div   @click="changeModal(1)" class="project grid1 grid-span">
                <img src="../assets/AOTSM.png">
                <h2>All around the state moving</h2>
                <p>Click to learn more</p>
                <p2>Click to learn more</p2>
                <div class="info-box">
                    <h3>All around the state moving</h3>
                    <p>All around the state moving is a website built for a Dallas based moving company</p>
                    <a href="https://www.icoconverter.com/" target="_blank">https://www.icoconverter.com</a>
                </div>
            </div>
            <div @click="changeModal(2)" class="project grid2 no-span">
                <img src="../assets/Demo1.png">
                <h2>Demo Website 1</h2>
                <p>Click to learn more</p>
                <p2>Click to learn more</p2>
                <div class="info-box">
                    <h3>Title</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus accusamus laboriosam aliquam illum in id rerum voluptate maxime, unde nobis sequi suscipit, possimus quam voluptatum, sit nulla accusantium saepe odio.</p>
                    <a href="https://www.icoconverter.com/" target="_blank">"LINK"</a>
                </div>
            </div>
            <div @click="changeModal(3)" class="project grid3 row-span">
                <img src="../assets/Demo4.png">
                <h2>Demo Website 4</h2>
                <p>Click to learn more</p>
                <p2>Click to learn more</p2>
                <div class="info-box">
                    <h3>Title</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus accusamus laboriosam aliquam illum in id rerum voluptate maxime, unde nobis sequi suscipit, possimus quam voluptatum, sit nulla accusantium saepe odio.</p>
                    <a href="https://demo4-duckweed.netlify.app/#home" target="_blank">https://demo4-duckweed.netlify.app</a>
                </div>
            </div>
            <div @click="changeModal(4)" class="project grid4 no-span">
                
                <img src="../assets/Demo2.png">
                <h2>Demo Website 2</h2>
                <p>Click to learn more</p>
                <p2>Click to learn more</p2>
                <div class="info-box">
                    <h3>Title</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus accusamus laboriosam aliquam illum in id rerum voluptate maxime, unde nobis sequi suscipit, possimus quam voluptatum, sit nulla accusantium saepe odio.</p>
                    <a href="https://www.icoconverter.com/" target="_blank">"LINK"</a>
                </div>
            </div>
            <div @click="changeModal(5)" class="project grid5 grid-span">
                
                <img src="../assets/Demo3.png">
                <h2>Demo Website 3</h2>
                <p>Click to learn more</p>
                <p2>Click to learn more</p2>
                <div class="info-box">
                    <h3>Title</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus accusamus laboriosam aliquam illum in id rerum voluptate maxime, unde nobis sequi suscipit, possimus quam voluptatum, sit nulla accusantium saepe odio.</p>
                    <a href="https://www.icoconverter.com/" target="_blank">"LINK"</a>
                </div>
            </div>
            <div @click="changeModal(6)" class="project grid6 row-span">
                <img src="../assets/Duckweed.png">
                <h2>Duckweed Marketing Website</h2>
                <p>Click to learn more</p>
                <p2>Click to learn more</p2>
                <div class="info-box">
                    <h3>Title</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus accusamus laboriosam aliquam illum in id rerum voluptate maxime, unde nobis sequi suscipit, possimus quam voluptatum, sit nulla accusantium saepe odio.</p>
                    <a href="https://duckweedmarketing.com" target="_blank">https://duckweedmarketing.com</a>
                </div>
            </div>
            <div @click="changeModal(7)" class="project grid7 no-span">
                <img src="../assets/Diner.jpg">
                <h2>Restaurant App (College Project)</h2>
                <p>Click to learn more</p>
                <p2>Click to learn more</p2>
                <div class="info-box">
                    <h3>Restaurant System (College Project)</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus accusamus laboriosam aliquam illum in id rerum voluptate maxime, unde nobis sequi suscipit, possimus quam voluptatum, sit nulla accusantium saepe odio.</p>
                    <a href="https://www.icoconverter.com/" target="_blank">"LINK"</a>
                </div>
            </div>
            <div @click="changeModal(8)" class="project grid8 grid-span">
                <img src="../assets/Karaoke.png">
                <h2>Karaoke on Wheel (In Progress)</h2>
                <p>Click to learn more</p>
                <p2>Click to learn more</p2>
                <div class="info-box">
                    <h3>Karaoke on Wheel (In Progress)</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus accusamus laboriosam aliquam illum in id rerum voluptate maxime, unde nobis sequi suscipit, possimus quam voluptatum, sit nulla accusantium saepe odio.</p>
                    <a href="https://www.icoconverter.com/" target="_blank">"LINK"</a>
                </div>
            </div>
            <div @click="changeModal(9)" class="project grid9 grid-span">
                <img src="../assets/Flash.png">
                <h2>Flash Card Web App (In Progress)</h2>
                <p>Click to learn more</p>
                <p2>Click to learn more</p2>
                <div class="info-box">
                    <h3>Title</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus accusamus laboriosam aliquam illum in id rerum voluptate maxime, unde nobis sequi suscipit, possimus quam voluptatum, sit nulla accusantium saepe odio.</p>
                    <a href="https://www.icoconverter.com/" target="_blank">"LINK"</a>
                </div>
            </div>
            <div @click="changeModal(10)" class="project grid10 no-span ">
                <img src="../assets/Diner.jpg">
                <h2>POS System (In Progress)</h2>
                <p>Click to learn more</p>
                <p2>Click to learn more</p2>
                <div class="info-box">
                    <h3>Title</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus accusamus laboriosam aliquam illum in id rerum voluptate maxime, unde nobis sequi suscipit, possimus quam voluptatum, sit nulla accusantium saepe odio.</p>
                    <a href="https://www.icoconverter.com/" target="_blank">"LINK"</a>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.grid[show-modal="1"] .grid2,
.grid[show-modal="1"]  .grid3,
.grid[show-modal="1"] .grid4,
.grid[show-modal="1"] .grid5,
.grid[show-modal="2"] .grid1,
.grid[show-modal="2"]  .grid3,
.grid[show-modal="2"] .grid4,
.grid[show-modal="2"] .grid5,
.grid[show-modal="3"] .grid2,
.grid[show-modal="3"]  .grid1,
.grid[show-modal="3"] .grid4,
.grid[show-modal="3"] .grid5,
.grid[show-modal="4"] .grid2,
.grid[show-modal="4"]  .grid3,
.grid[show-modal="4"] .grid1,
.grid[show-modal="4"] .grid5,
.grid[show-modal="5"] .grid2,
.grid[show-modal="5"]  .grid3,
.grid[show-modal="5"] .grid4,
.grid[show-modal="5"] .grid1,
.grid[show-modal="6"] .grid7,
.grid[show-modal="6"] .grid8,
.grid[show-modal="6"] .grid9,
.grid[show-modal="6"] .grid10,
.grid[show-modal="7"] .grid6,
.grid[show-modal="7"] .grid8,
.grid[show-modal="7"] .grid9,
.grid[show-modal="7"] .grid10,
.grid[show-modal="8"] .grid6,
.grid[show-modal="8"] .grid7,
.grid[show-modal="8"] .grid9,
.grid[show-modal="8"] .grid10,
.grid[show-modal="9"] .grid6,
.grid[show-modal="9"] .grid7,
.grid[show-modal="9"] .grid8,
.grid[show-modal="9"] .grid10,
.grid[show-modal="10"] .grid6,
.grid[show-modal="10"] .grid7,
.grid[show-modal="10"] .grid8,
.grid[show-modal="10"] .grid9
{
    display: none;
}
.grid[show-modal="1"] .grid1,
.grid[show-modal="2"] .grid2,
.grid[show-modal="3"] .grid3,
.grid[show-modal="4"] .grid4,
.grid[show-modal="5"] .grid5,
.grid[show-modal="6"] .grid6,
.grid[show-modal="7"] .grid7,
.grid[show-modal="8"] .grid8,
.grid[show-modal="9"] .grid9,
.grid[show-modal="10"] .grid10{
    grid-column:span  4;
    grid-row: span 2;
}

/**Info Box Styles */
.info-box{
    position: absolute;
    width: 100%;
    height: 100%;
    opacity: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
}
.info-box a{
    text-decoration: none;
    color: rgb(30, 30, 30);
    font-size: 17px;
}
.info-box h3{
    font-size: 30px;
}
.info-box p{
    font-size:15px;
}
.grid[show-modal="1"] .grid1 .info-box,
.grid[show-modal="2"] .grid2 .info-box,
.grid[show-modal="3"] .grid3 .info-box,
.grid[show-modal="4"] .grid4 .info-box,
.grid[show-modal="5"] .grid5 .info-box,
.grid[show-modal="6"] .grid6 .info-box,
.grid[show-modal="7"] .grid7 .info-box,
.grid[show-modal="8"] .grid8 .info-box,
.grid[show-modal="9"] .grid9 .info-box,
.grid[show-modal="10"] .grid10 .info-box{

    background-color: inherit;
    opacity: 20;
    z-index: 16;
}

.container{
    width: 100%;
    height: 1500px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    background-color:  rgb(30, 30, 30);
    border-top: solid 4px var(--secondary-yellow);
    border-bottom: solid 4px var(--secondary-yellow);
}
.container h1{
    font-size: 100px;
    color: var(--main-white);
}
.grid{
    width: 80%;
    height: 60%;
    display: grid;
    color: var(--main-white);
    grid-template-columns: repeat(4,1fr);
    grid-template-rows: repeat(4,1fr);
    gap:1rem;
    transition: all 1s ease;
}
.project{
    background-color: var(--main-yellow);
    border-radius: 2px;
    transition:all .4s ease;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    position: relative;
    transition: all 1s ease;
}
.project img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    position:absolute;
    opacity: 0;
    transition: all .4s ease;
    object-position: 0% 0%;
}
.project:hover img{
    opacity:1;
}

.project p2{
    opacity:0;
    transition:all .2s ease;
}
.project:hover p2{
    z-index: 15;
    font-size:20px;
    background-color: inherit;
    opacity: 1;
    border-radius: 5px;
    padding:2%;
}
.project p2:hover{
    transform: scale(1.02);
}

.project h2{
    font-size:30px;
}
.grid[show-modal="0"] .project:hover{
    transform:scale(1.02);
}
.grid-span{
    grid-column:span 2;
}
.grid-span img{
    object-position: 50% 0%;
}
.row-span{
    grid-row:span 2;
}
.grid1,.grid6, .grid8{
    background-color: var(--main-orange);

}
.grid2,.grid5,.grid9{
    background-color: var(--secondary-yellow);
}
.grid3,.grid4,.grid7,.grid10{
    background-color: var(--main-yellow);
}


@media (min-width: 1024px) {
  
}
@media (max-width: 1023px) and (min-width:480px){

}
@media (max-width: 480px){
  
}
</style>
