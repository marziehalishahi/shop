<script setup>
import { ref } from 'vue'
import { UserIcon, MagnifyingGlassIcon, ShoppingCartIcon, ChevronDownIcon } from '@heroicons/vue/24/outline'

</script>

<template>
    <nav class="menubar">
        <div class="menubar__logo">
            <img src="../assets/images/images.svg">
        </div>
        <div>
            <ul class="menubar__items">
                <li>Men</li>
                <li>Women</li>
                <li>Beauty</li>
                <li>Sport</li>
                <li>Templates <ChevronDownIcon class="w-4 h-4 text-gray-400 inline-block"/></li>
                <li>Explore</li>
            </ul>
        </div>

        <div class="menubar__interactions">
            <div>
                <UserIcon class="w-8 h-8 text-black"></UserIcon>
            </div>
            <div>
                <MagnifyingGlassIcon class="w-8 h-8 text-black"></MagnifyingGlassIcon>
            </div> 
            <div class="menubar__shopping_cart">
                <ShoppingCartIcon class="w-8 h-8 text-black">

                </ShoppingCartIcon>
                <div class="menubar__shopping_cart_count menubar__shopping_cart--position">1</div>
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
.menubar__logo img{
    object-fit: cover;
    width: auto;
    height: 90px;
}
.menubar__items{
    display: flex;
    justify-content: center;
    gap: 30px;
    font-size: 1.8rem;
    font-weight: 400;
}
.menubar__items li:nth-child(5):hover{
    cursor: pointer;
}
.menubar__interactions{
    display: flex;
    justify-content: center;
    gap: 30px;
    font-size: 1.8rem;
    font-weight: 400;
}
.menubar__shopping_cart{
    position: relative;
}
.menubar__shopping_cart_count{
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
.menubar__shopping_cart--position{
    display: flex;
    align-items: center;
    justify-content: center;
}
</style>
