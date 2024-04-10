<script>
import AppTitle from './AppTitle.vue';
export default {
    name: 'AppHero',
    components: {
        AppTitle
    },
    data() {
        return {
            image: ''
        }
    },
    methods: {
        printRelaxImg() {
            this.image = 'src/assets/img/spiderman.jpg'
        },
        printPartyImg() {
            this.image = ''
        }
    }
}
</script>

<template>
    <div class="hero-bg">
        <AppTitle></AppTitle>
        <img :src="image">
        <div>
            <button @click="printRelaxImg()">Click to relax</button>
            <button @click="printPartyImg()">Click to party</button>
        </div>
    </div>
</template>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.hero-bg {
    background-image: url(../assets/img/marvel.jpg);
    background-position: center;
    width: 100vw;
    height: 100vh;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
}

button {
    margin-block: 20px;
    margin-right: 20px;
    padding: 6px;
    width: fit-content;
    height: 30px;
    border: none;
    border-radius: 6px;
    box-shadow: 4px 4px #ffffff60;
    cursor: pointer;
}

img {
    height: calc(100vh - 150px);
}
</style>
