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

        <div @click.out="cart = false"  class="shopping_cart__details--hidden" :class="{ 'shopping_cart__details shadow-md': cart }">
            <div class="h-[350px] overflow-y-scroll ">
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
            <div class="shopping_cart__sumary summary">
                <div class="summary__total">
                    <span class="summary__font">Subtotal</span>
                    <span class="summary_price">$220</span>
                </div>
                <p class="shpping_cart__description">
                    A simple static page
                </p>
                <div class="summary__cta cta">
                    <a class="cta__view">View cart</a>
                    <span class="mx-6"></span>
                    <a class="cta__checkout">Checkout</a>
                </div>
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
    background-color: azure;
    border-radius: 100%;
}

.shopping_cart__details--hidden {
    display: none;
}

.shopping_cart--height {
    height: auto;
}

.shopping_cart__header {
    font-size: 1.7rem;
    font-weight: 400;
}

.shopping_cart__elements img {
    border-radius: 30px;
}

.summary__total{
    display: flex;
    justify-content: space-between;
    font-weight: bold;
    color: black;

}
.shopping_cart__sumary 
{
    padding: 1rem;
    background-color: rgb(233, 246, 248)
}
.summary__cta
{
    margin-top: 20px;
    text-align: center;
}
.cta__view
{
    border: 1px solid none;
    border-radius: 18px;
    padding: 15px 0;
    display: inline-block;
    width: 40%;
    background-color: white;
    transform: scale(1,1);
    transition: all 100ms linear;
    color: black;
    outline: none;
}

.cta__view:hover
{
    border-radius: 18px;
    padding: 15px 0;
    display: inline-block;
    width: 40%;
    background-color: rgb(74, 74, 97);
    color: white;
    border: none;
    outline: none;
    transform: scale(1.1, 1.1);
}
.cta__view:active
{
    background-color: rgb(74, 74, 97);
    border: 1px solid black;
}

.cta__checkout
{
    border: 1px solid gray;
    border-radius: 18px;
    padding: 15px 0;
    display: inline-block;
    width: 40%;
    background-color: rgb(74, 74, 97);
    color: white;
    transition: all 100ms linear;
    transform: scale(1, 1);

}
.cta__checkout:hover{
    background-color: white;
    border:none ;
    color:rgb(5, 28, 49) ;
    transform: scale(1.1, 1.1);
    
}

.shopping_cart__details {
    width: 500px;
    height: 500px;
    background-color: white;
    position: absolute;
    top: 40px;
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
    background-color: rgb(145, 178, 240);
    color: white;
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