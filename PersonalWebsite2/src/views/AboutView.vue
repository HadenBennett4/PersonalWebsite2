<script setup>
import { ref } from 'vue'

const show = ref("false");

function changeShow() {
    if (show.value === "false") {
        show.value = "true";
    } else {
        show.value = "false";
    }
}
</script>

<template>
    <div class="container">
        <div class="wrapper">
            <div class="orange"></div>
            <div class="yellow"></div>
            <div class="sec-yellow"></div>
            <div></div>
            <div></div>
            <div></div>
            <div :showThis=[show] class="about">
                <div class="about-header">
                    <h1>ABOUT ME</h1>
                    <div @click="changeShow()" class="close-open-button">Learn More</div>
                </div>
                <div class="about-info">
                    <h1>A Little About Me</h1>
                    <p>My name is Haden Bennett. I am a highly dedicated freelance front end developer and designer.
                        I graduated form the University Of North Texas with a degree in Computer Science. Feel free to check out my projects
                        and follow me on Linkedin!!
                    </p>
                    <div @click="changeShow()" class="close-open-button">Close</div>
                </div>
            </div>
            <div class="sec-yellow"></div>
            <div class="yellow"></div>
            <div class="orange"></div>
        </div>
    </div>
</template>

<style scoped>
@media (min-width: 1024px) {
    .container {
        width: 100%;
        height: 700px;
        border-top: solid 4px var(--secondary-yellow);
    }

    .wrapper {
        width: 100%;
        height: 100%;
        display: grid;
        grid-template-rows: repeat(9,1fr);
        overflow-x: hidden;
        overflow-y: hidden;
        position: relative;
    }

    .orange,
    .yellow,
    .sec-yellow {
        width: 100%;
        height: 100%;
        z-index: -4;
        transform-origin: 50%;

    }
    .orange {
        background-color: var(--main-orange);
    }
    .yellow {
        background-color: var(--main-yellow);
    }
    .sec-yellow {
        background-color: var(--secondary-yellow);
    }

    .about {
        width: 400%;
        height: 70%;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        rotate:-10deg;
        transform: translate(-4%,-45%);
        transition: all 1.5s ease;
        box-shadow: 0 0 0 4px var(--main-yellow),
            0 0 0 8px var(--main-orange),
            0 0 0 12px var(--secondary-yellow);
        position: absolute;
    }

    .about-info, .about-header {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        transition: all 1s ease;
        background-color: rgb(30, 30, 30);
        text-align: center;
    }

    .about-info {
        grid-column-start: 2;
        margin-left: -1%;
    }

    .about-header {
        grid-column-start: 1;
    }

    .about[showThis="true"] .about-header {
        transform: translateX(-100%);
    }

    .about[showThis="true"] .about-info {
        transform: translateX(-100%);
    }

    .about-header h1, .about-info h1{
        color:var(--main-white);
        font-size: 40px;
    }
    .about-info p {
        color:var(--main-white);
        font-size: 20px;
        width: 50%;
    }
    .close-open-button{
        padding: 1%;
        background-color: var(--main-white);
        width: 10%;
        height: 5%;
        font-size: 20px;
        font-weight: bold;
        border-radius: 5px;
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        transition: all .3s ease;
    }
    .close-open-button:hover{
        transform: scale(1.01);
    }


}

@media (max-width: 1023px) and (min-width:480px) {

    .container {
        width: 100%;
        height: 50em;
        border-top: solid 4px var(--secondary-yellow);
    }

    .wrapper {
        width: 100%;
        height: 100%;
        display: grid;
        grid-template-rows: repeat(9,1fr);
        overflow-x: hidden;
        overflow-y: hidden;
        position: relative;
    }

    .orange,
    .yellow,
    .sec-yellow {
        width: 100%;
        height: 100%;
        z-index: -4;

    }
    .orange {
        background-color: var(--main-orange);
    }
    .yellow {
        background-color: var(--main-yellow);
    }
    .sec-yellow {
        background-color: var(--secondary-yellow);
    }

    .about {
        width: 400%;
        height: 60%;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        transition: all 1.5s ease;
        transform: translate(-4%,33%);
        box-shadow: 0 0 0 4px var(--main-yellow),
            0 0 0 8px var(--main-orange),
            0 0 0 12px var(--secondary-yellow);
        position: absolute;
        transform-origin: 50%;;
    }

    .about-info, .about-header {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        transition: all 1s ease;
        background-color: rgb(30, 30, 30);
        text-align: center;
    }

    .about-info {
        grid-column-start: 2;
    }

    .about-header {
        grid-column-start: 1;
    }

    .about[showThis="true"] .about-header {
        transform: translateX(-100%);
    }

    .about[showThis="true"] .about-info {
        transform: translateX(-100%);
    }

    .about-header h1, .about-info h1{
        color:var(--main-white);
        font-size: 40px;
    }
    .about-info p {
        color:var(--main-white);
        font-size: 20px;
        width: 50%;
    }
    .close-open-button{
        padding: 1%;
        background-color: var(--main-white);
        width: 15%;
        height: 10%;
        font-size: 20px;
        font-weight: bold;
        border-radius: 5px;
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        transition: all .3s ease;
    }

}

@media (max-width: 480px) {

    .container {
        width: 100%;
        height: 700px;
        border-top: solid 4px var(--secondary-yellow);
    }

    .wrapper {
        width: 100%;
        height: 100%;
        display: grid;
        grid-template-rows: repeat(9,1fr);
        overflow-x: hidden;
        overflow-y: hidden;
        position: relative;
    }

    .orange,
    .yellow,
    .sec-yellow {
        width: 100%;
        height: 100%;
        z-index: -4;
        transform-origin: 50%;

    }
    .orange {
        background-color: var(--main-orange);
    }
    .yellow {
        background-color: var(--main-yellow);
    }
    .sec-yellow {
        background-color: var(--secondary-yellow);
    }

    .about {
        width: 400%;
        height: 70%;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        rotate:-10deg;
        transform: translate(-4%,-45%);
        transition: all 1.5s ease;
        box-shadow: 0 0 0 4px var(--main-yellow),
            0 0 0 8px var(--main-orange),
            0 0 0 12px var(--secondary-yellow);
        position: absolute;
    }

    .about-info, .about-header {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        transition: all 1s ease;
        background-color: rgb(30, 30, 30);
        text-align: center;
    }

    .about-info {
        grid-column-start: 2;
        margin-left: -1%;
    }

    .about-header {
        grid-column-start: 1;
    }

    .about[showThis="true"] .about-header {
        transform: translateX(-100%);
    }

    .about[showThis="true"] .about-info {
        transform: translateX(-100%);
    }

    .about-header h1, .about-info h1{
        color:var(--main-white);
        font-size: 40px;
    }
    .about-info p {
        color:var(--main-white);
        font-size: 20px;
        width: 50%;
    }
    .close-open-button{
        padding: 1%;
        background-color: var(--main-white);
        width: 10%;
        height: 5%;
        font-size: 20px;
        font-weight: bold;
        border-radius: 5px;
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        transition: all .3s ease;
    }
    .close-open-button:hover{
        transform: scale(1.01);
    }

}
</style>
