<script setup>
import { ref } from 'vue'
import { UserIcon, MagnifyingGlassIcon, ShoppingCartIcon } from '@heroicons/vue/24/outline'

</script>

<template>
    <nav class="menubar">
        <div class="menubar_logo">
            <img src="../assets/images/images.svg">
        </div>
        <div>
            <ul class="menubar_items">
                <li>Men</li>
                <li>Women</li>
                <li>Beauty</li>
                <li>Sport</li>
                <li>Templates</li>
                <li>Explore</li>
            </ul>
        </div>

        <div class="menubar_interactions">
            <div>
                <UserIcon class="w-8 h-8 text-black"></UserIcon>
            </div>
            <div>
                <MagnifyingGlassIcon class="w-8 h-8 text-black"></MagnifyingGlassIcon>
            </div> 
            <div class="shopping_cart">
                <ShoppingCartIcon class="w-8 h-8 text-black">

                </ShoppingCartIcon>
                <span class="shopping_cart_count"><span style="margin-top: 1px;">1</span></span>
            </div>
        </div>
    </nav>
</template>

<style scoped>

nav.menubar {
    width: 100%;
    background-color: white;
    display: flex;
    justify-content: space-around;
    align-items: center;
    height: 100px;
}
.menubar_logo img{
    object-fit: cover;
    width: auto;
    height: 90px;
}
.menubar_items{
    display: flex;
    justify-content: center;
    gap: 30px;
    font-size: 1.8rem;
    font-weight: 400;
}
.menubar_interactions{
    display: flex;
    justify-content: center;
    gap: 30px;
    font-size: 1.8rem;
    font-weight: 400;
}
.shopping_cart{
    position: relative;
}
.shopping_cart_count{
    position: absolute;
    text-align: center;
    background-color: aqua;
    color: black;   
    border-radius: 100%;
    width: 20px;
    height: 20px;
    font-size: .7rem;
    right: -7px;
    top: -6px;
}
</style>
