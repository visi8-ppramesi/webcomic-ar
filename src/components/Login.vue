<template>
    <div class="background">
        <div class="spacer">

        </div>
        <div class="flex-col justify-center align-center relative">
            <router-link to="/dashboard"><img src="../assets/signin.png" alt=""></router-link>
            <router-link to="/dashboard"><img src="../assets/signup.png" alt=""></router-link>
            <router-link to="/dashboard"><img src="../assets/social.png" alt=""></router-link>
        </div>
    </div>
</template>

<script>
import {ref} from 'vue'
export default{
    name: 'login',
    created(){
        console.log('asdfasdasdf')
    }
}
</script>

<style lang="postcss">
.relative{
    position: relative;
}
.background{
    position:relative;
    max-width: 1200px;
    height: 100vh;
}
.background:before{
    content: '';
    position:absolute;
    top: 0px;
    right: 0px;
    bottom: 0px;
    left: 0px;
    /* max-width: 1200px; */
    /* height: 100vh; */
    background:
        url(../assets/Logo.png) calc(50vw - 40px) calc(10vh)/190px 160px no-repeat,
        url(../assets/bg1.png) calc(100% + 20px) calc(100% - 20px)/calc(75vw) calc(75vw) no-repeat,
        url(../assets/bg2.png) calc(100% - 140px) calc(100% - 20px)/calc(75vw) calc(75vw) no-repeat,
        url(../assets/bg3.png) calc(100% + 25px) calc(100% - 80px)/calc(100vw + 100px) calc(100vw + 100px) no-repeat;
    opacity: 0.5;
}
.spacer{
    height: 50vh;
}
</style>