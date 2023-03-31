<script setup>
import { ref, onMounted } from 'vue'
import { UserIcon, MagnifyingGlassIcon, ShoppingCartIcon, ChevronDownIcon } from '@heroicons/vue/24/outline'

onMounted(() => {
    document.querySelector('.menubar__templates').addEventListener('mouseenter', function (event) {
        document.querySelector('.menubar__megamenu').style.display = 'block'
    })
    document.querySelector('.menubar__templates').addEventListener('mouseleave', function (event) {
        document.querySelector('.menubar__megamenu').style.display = 'none'
    })
})


</script>

<template>
    <nav class="menubar">
        <div class="menubar__logo">
            <img src="../assets/images/images.svg">
        </div>
        <div class="flex items-center h-full">
            <ul class="h-full menubar__items">
                <li>Men </li>
                <li>Women</li>
                <li>Beauty</li>
                <li>Sport</li>
                <li>
                    <div class="menubar__templates"><span> Templates</span>
                        <ChevronDownIcon class="inline-block w-4 h-4 text-gray-400" />
                    </div>
                </li>
                <li>
                    <div class="menubar__explore">
                        <span>Explore </span>
                        <ChevronDownIcon class="inline-block w-4 h-4 text-gray-400" />
                        <ul class="menubar__explore--items">
                            <li>Men </li>
                            <li class="relative">Women  <ChevronDownIcon class="inline-block w-4 h-4 text-gray-400" />
                                <ul class="absolute right-[-40px] w-20 bg-black h-36"></ul>
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
    <div class="menubar__megamenu"></div>
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

.menubar__items li {
    padding: .5rem 1rem;
}

/* body .menubar__templates:hover ~ .menubar__megamenu{
    display: block;
} */
.menubar__items li:hover {
    cursor: pointer;
    background-color: azure;
    border-radius: 2rem;
}

.menubar__interactions {
    display: flex;
    justify-content: center;
    gap: 30px;
    font-size: 1.8rem;
    font-weight: 400;

}

.menubar__shopping_cart {
    position: relative;
}

.menubar__shopping_cart_count {
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

.menubar__shopping_cart--position {
    display: flex;
    align-items: center;
    justify-content: center;
}
.menubar__explore{
    position: relative;
}
.menubar__explore:hover .menubar__explore--items{
    height: auto;
    width: 120px;
}
.menubar__explore:hover .menubar__explore--items li{
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
.menubar__explore--items li {
    font-size: .8rem;
    opacity: 0;
    transition-delay: 100ms;
    display: flex;
    justify-content: space-between;
}
.menubar__megamenu {
    position: absolute;
    width: 100%;
    height: 300px;
    background-color: white;
    top: 0;
    margin-top: 100px;
    display: none;
}

</style>
