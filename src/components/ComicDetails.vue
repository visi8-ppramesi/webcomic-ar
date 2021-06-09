<template>
    <div class="p-1">
        <div style="position:relative">
            <router-link to="/view" class="read-button">
                <img src="../assets/Read.png" alt="">
            </router-link>
            <img src="../assets/Kara_Book_Info.png" alt="" class="pr-2">
        </div>
        <div class="px-4">
            Comments
        </div>
        <img src="../assets/Comment01.png" alt="" class="pr-2">
        <img src="../assets/Comment02.png" alt="" class="pr-2">
    </div>
</template>

<script>
import {ref} from 'vue'
export default{
    name: 'comic-details',
    created(){
        console.log('asdfasdasdf')
    }
}
</script>

<style lang="postcss">
.read-button{
    position: absolute;
    z-index: 999;
    width: 25vw;
    top: 23%;
    right: 1rem;
}
</style>