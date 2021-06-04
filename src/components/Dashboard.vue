<template>
    <div class="p-1">
        <div>
            <img src="../assets/search.png">
            <!-- <input class="bg-gray-800 shadow appearance-none rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="Search a book">  -->
        </div>
        <div class="grid grid-cols-2 gap-4">
            <router-link to="/details"><img src="../assets/1.png"></router-link>
            <img src="../assets/2.png">
            <img src="../assets/3.png">
            <img src="../assets/4.png">
            <img src="../assets/3.png">
            <img src="../assets/4.png">
            <img src="../assets/3.png">
            <img src="../assets/4.png">
            <img src="../assets/3.png">
        </div>
    </div>
</template>

<script>
import {ref} from 'vue'
export default{
    name: 'dashboard',
    created(){
        console.log('asdfasdasdf')
    },
    data(){
        return {
        }
    }
}
</script>

<style lang="postcss">

</style>