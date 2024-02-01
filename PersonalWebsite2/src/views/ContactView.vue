<template>
    <div class="container">
        <div class="wrapper">
            <div class="orange"></div>
            <div class="yellow"></div>
            <div class="sec-yellow"></div>
            <div></div>
            <div></div>
            <div></div>
            <div class="about">
                    <h1>Contact Me</h1>
                    <div class="info-row">
                        <div class="icon-container">                  
                                <v-icon class="icon" name="co-linkedin" scale="8"></v-icon>
                                <h2>Linkedin</h2>             
                        </div>
                        <div class="icon-container">             
                                <v-icon class="icon" name="fa-github-square" scale="8"></v-icon>
                                <h2>Github</h2>          
                        </div>
                        <div class="icon-container">                    
                                <v-icon class="icon" name="md-email" scale="8"></v-icon>
                                <h2>Email</h2>
                        </div>
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
    }

    .wrapper {
        width: 100%;
        height: 100%;
        display: grid;
        grid-template-rows: repeat(9, 1fr);
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
        width: 150%;
        height: 70%;
        rotate: 10deg;
        transform: translate(-15%, 32%);
        transition: all 1.5s ease;
        box-shadow: 0 0 0 4px var(--main-yellow),
            0 0 0 8px var(--main-orange),
            0 0 0 12px var(--secondary-yellow);
        position: absolute;
        background-color: rgb(30, 30, 30);
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-around;
    }
    .about h1{
        color: var(--main-white);
        font-size:50px;
    }
    .info-row{
        margin-bottom: 40px;
        width:60%;
        height:70%;
        display: grid;
        grid-template-columns: repeat(3,1fr);
        gap:1rem;
    }
    .icon-container{
       border:5px solid var(--main-white);
       border-radius: 10px;
       display: grid;
       grid-template-rows:1.5fr 1fr;
       transition: all .5s ease;
    }
    .icon-container:hover{
        transform: scale(1.02);
    }
    .icon-container h2{
        color: white;
        font-size: 40px;
        margin:0 auto;
    }
    .icon{
        fill:white;
        margin:0 auto;
    }


}

@media (max-width: 1023px) and (min-width:480px) {}

@media (max-width: 480px) {}</style>
