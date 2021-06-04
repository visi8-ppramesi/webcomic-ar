<template>
    <div>
        <img id="ar-1" src="../assets/comic/01-SLEEPING_AR.jpg">
        <img src="../assets/comic/02-WAKING_UP.jpg">
        <img id="ar-2" src="../assets/comic/03-KARA_HOUSE_AR.jpg">
        <img id="ar-3" src="../assets/comic/04-KARA_WINDOW_AR.jpg">
        <img src="../assets/comic/05-KARA_WRITING.jpg">
        <img id="ar-4" src="../assets/comic/06-KARA_LUNA_AR.jpg">
        <img src="../assets/comic/07-KARA_LUNA_TABLE.jpg">
    </div>
    <div class="tester">
        <div v-show="b1">
            <router-link to="/">
                <img src="../assets/Record.png" alt="">
            </router-link>
        </div>
        <div v-show="b2">
            <router-link to="/">
                <img src="../assets/Record.png" alt="">
            </router-link>
        </div>
        <div v-show="b3">
            <router-link to="/">
                <img src="../assets/Record.png" alt="">
            </router-link>
        </div>
        <div v-show="b4">
            <router-link to="/">
                <img src="../assets/Record.png" alt="">
            </router-link>
        </div>
    </div>
</template>

<script>
import {ref} from 'vue'
export default{
    name: 'comic-view',
    created(){
        window.addEventListener('scroll', this.handleScroll)
    },
    mounted(){
        const ar1 = document.getElementById('ar-1')
        const ar2 = document.getElementById('ar-2')
        const ar3 = document.getElementById('ar-3')
        const ar4 = document.getElementById('ar-4')
        if(this.isInViewport(ar1)){
            this.b1 = true
        }else{
            this.b1 = false
        }

    },
    data(){
        return {
            b1: false,
            b2: false,
            b3: false,
            b4: false
        }
    },
    methods:{
        handleScroll(){
            const ar1 = document.getElementById('ar-1')
            const ar2 = document.getElementById('ar-2')
            const ar3 = document.getElementById('ar-3')
            const ar4 = document.getElementById('ar-4')
            if(this.isInViewport(ar1)){
                this.b1 = true
            }else{
                this.b1 = false
            }
            if(this.isInViewport(ar2)){
                this.b2 = true
            }else{
                this.b2 = false
            }
            if(this.isInViewport(ar3)){
                this.b3 = true
            }else{
                this.b3 = false
            }
            if(this.isInViewport(ar4)){
                this.b4 = true
            }else{
                this.b4 = false
            }
        },
        isInViewport(element) {
            const rect = element.getBoundingClientRect();
            return (
                rect.top >= 0 &&
                rect.left >= 0 &&
                rect.bottom <= (window.innerHeight || document.documentElement.clientHeight) &&
                rect.right <= (window.innerWidth || document.documentElement.clientWidth)
            );
        }
    }
}
</script>

<style lang="postcss">
.tester{
    position: fixed;
    z-index: 9999;
    bottom: 0;
    left: calc(50% - 62px);
}
</style>