<script setup>

</script>
<template>
    <div class="container">
        <div class="wrapper">
            <h1></h1>
            <p></p>
            <a href=""></a>
            <div class="back-button">Close</div>
        </div>
    </div>
</template>
<style scoped>
.container {
    position:absolute;
    width: 100%;
    height: 110%;
    background-color: rgb(0,0,0,.5);
    z-index: 150;
}
.wrapper{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-evenly;
    position: relative;
    background-color: var(--main-orange);
    width: 50%;
    height: 50%;
}
</style>