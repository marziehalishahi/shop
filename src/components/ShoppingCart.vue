<script setup>
import { ShoppingCartIcon } from '@heroicons/vue/24/outline'
import { ref, onMounted } from 'vue'
import ShoppingCartItems from '@/ShoppingCartItems.vue'

let cart = ref(false);
const toggleCart = () => {
    cart.value = !cart.value;
}
</script>

<template>
    <div @click="toggleCart" class="menubar__shopping_cart shopping_cart">

        <div class='shopping_cart__background'>
            <ShoppingCartIcon class="w-6 h-6 text-black">

            </ShoppingCartIcon>
        </div>

        <div class="shopping_cart__count shopping_cart--position">1</div>

        <div class="shopping_cart__details--hidden" :class="{ 'shopping_cart__details shadow-md': cart }">
            <div class="h-[400px] overflow-y-scroll ">
                <div class="shopping_cart__padding">
                    <div class="shopping_cart--height">
                        <h3 class="shopping_cart__header">Your products</h3>
                        <ShoppingCartItems image="../../images/2.jpg"></ShoppingCartItems>
                        <ShoppingCartItems image="../../images/3.jpg"></ShoppingCartItems>
                        <ShoppingCartItems image="../../images/4.jpg"></ShoppingCartItems>
                        <ShoppingCartItems image="../../images/5.jpg"></ShoppingCartItems>
                        <ShoppingCartItems image="../../images/6.jpg"></ShoppingCartItems>                       
                    
                    </div>
                </div>

            </div>
            <div>
                sadsfsdfsdf;sljkdf;lsjkaf
            </div>
        </div>
    </div>
</template>

<style scoped>
.shopping_cart__padding {
    /* border: 1px solid black; */
    margin: .5rem 1rem;
    height: auto;
}

.menubar__shopping_cart {
    position: relative;
    cursor: pointer;
}

.shopping_cart__background {
    padding: 10px;
}

.shopping_cart__background:hover {
    background-color: rgb(255, 255, 244);
    border-radius: 100%;
}

.shopping_cart__details--hidden {
    display: none;
}

.shopping_cart--height {
    height: auto;
}

.shopping_cart__header {
    font-size: 2rem;
    font-weight: bold;
}

.shopping_cart__elements img {
    border-radius: 30px;
}






.shopping_cart__details {
    width: 500px;
    height: 600px;
    background-color: white;
    position: absolute;
    bottom: -400px;
    left: -469px;
    /* box-shadow: 3px 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1); */
    display: block;
    font-size: 1rem;
    border-radius: 15px;
}

/* .shopping_cart__details::-webkit-scrollbar-thumb, .shopping_cart__details::-webkit-scrollbar-track, shopping_cart__details::-webkit-scrollbar, .shopping_cart__details::-webkit-scrollbar-track-piece{
    display: none;
} */


.shopping_cart__count {
    position: absolute;
    text-align: center;
    background-color: aqua;
    color: black;
    border-radius: 100%;
    width: 15px;
    height: 15px;
    font-size: .7rem;
    right: 0px;
    top: 5px;
}

.shopping_cart--position {
    display: flex;
    align-items: center;
    justify-content: center;
}</style>