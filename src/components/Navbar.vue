<script setup>
import ShoppingCart from '@/ShoppingCart.vue'
import { UserIcon, MagnifyingGlassIcon, ShoppingCartIcon, ChevronDownIcon } from '@heroicons/vue/24/outline'
import Megamenu from '@/Megamenu.vue'

// onMounted(()=>{console.log(cart.value ? 'yeds' : 'ndo')})
</script>

<template>
    <nav class="menubar">
        <div class="menubar__logo">
            <img src="../assets/images/images.svg">
        </div>
        <div class="flex items-center h-full">
            <ul class="h-full menubar__items">
                <li class="menubar__list"><span class="menubar__background">Men</span> </li>
                <li class="menubar__list"><span class="menubar__background">Women </span> </li>
                <li class="menubar__list"><span class="menubar__background">Beauty</span> </li>
                <li class="menubar__list"><span class="menubar__background">Sport </span> </li>
                <li class="menubar__list menubar__list--megamenu">
                    <div 
                     class="menubar__templates">
                        <span class="menubar__background"> Templates
                        <ChevronDownIcon class="inline-block w-4 h-4 text-gray-400" />
                    </span>
                    </div>
                    
                    <Megamenu></Megamenu>
                </li>
                <li class="menubar__list menubar_list--explore">
                    <div class="menubar__explore">
                        <span class="menubar__background">Explore 
                            <ChevronDownIcon class="inline-block w-4 h-4 text-gray-400" />
                        </span>
                        <ul class="menubar__explore--items">
                            <li>Men </li>
                            <li>Women
                                <ChevronDownIcon class="inline-block w-4 h-4 text-gray-400" />
                                <ul class="menubar__items--subtype"></ul>
                            </li>
                            <li>Beauty</li>
                            <li>Sport</li>
                        </ul>
                    </div>
                </li>
            </ul>
        </div>

        <div class="menubar__interactions">
            <div>
                <UserIcon class="w-6 h-6 text-black"></UserIcon>
            </div>
            <div>

                <MagnifyingGlassIcon class="w-6 h-6 text-black"></MagnifyingGlassIcon>

            </div>
            <ShoppingCart/>
        </div>

    </nav>
</template>

<style scoped>
nav.menubar {
    background-color: white;
    display: flex;
    justify-content: space-around;
    align-items: center;
    height: 100px;
    max-width: 1200px;
    margin: 0 auto;
    /* border-bottom: 1px solid lightgray; */
}

.menubar__logo {
    width: 130px;
}

.menubar__logo img {
    object-fit: contain;
    width: 100%;
    height: 90px;
}

.menubar__items {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 30px;
    font-size: 1.2rem;
    font-weight: 500;
}
span.menubar__background:hover{
    cursor: pointer;
    background-color: azure;
    border-radius: 2rem;
}
span.menubar__background{
    padding: .5rem 1rem;
}
li.menubar__list{
    display: flex;
    align-items: center;
    height: 100%;
}

.menubar__interactions {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 30px;
    font-size: 1.8rem;
    font-weight: 400;
}



.menubar__explore{
    position: relative;
}
.menubar_list--explore:hover .menubar__explore--items{
    height: auto;
    width: 120px;
}
.menubar_list--explore:hover .menubar__explore--items li{
    opacity: 1;
}
ul.menubar__explore--items{
    position: absolute;
    height: 0px;
    width: 0px;
    background-color: white;
    box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
    transition: all 100ms ease-in-out;
    transition-delay: 100ms;
    top: 40px;
}
.menubar__list.menubar__list--megamenu:hover .menubar__megamenu{
    transform: scale(1, 1);
    transform-origin: top center;
}

.menubar__explore--items li {
    font-size: .8rem;
    opacity: 0;
    transition-delay: 100ms;
    display: flex;
    justify-content: space-between;
    padding: 4px 8px;
}

.menubar__explore--items li:hover {
    background-color: aqua;
    cursor: pointer;
}
ul.menubar__items--subtype{
    position: absolute;
    right: -151px;
    width: 150px;
    transform: scale(0, 1);
    transition: transform 100ms ease-in-out;
    transform-origin: left center;
    background-color: black;
    height: 100px;
}
.menubar__explore--items li:hover ul.menubar__items--subtype{
    transform: scale(1, 1)
}


</style>
