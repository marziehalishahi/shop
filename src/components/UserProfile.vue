<script setup>
import { ref } from 'vue';
import { UserIcon } from '@heroicons/vue/24/outline';
let profile = ref(false)
function toggle() {
    profile.value = !profile.value
}

</script>


<template>
    <UserIcon @click="toggle" class= "w-6 h-6 p-0 text-black rounded-full cursor-pointer hover:bg-sky-100"></UserIcon>
    <div class="relative">
        <div :class="{ 'hidden': !profile }" class="absolute h-auto text-black bg-white rounded-lg shadow-md text w-36 top-8">
            <div class="flex justify-center">
                <div class=" flex flex-col gap-[2px] items-center h-auto w-auto p-[2rem] cursor-pointer mx-0 my-3 text-justify ">
                    <div class="UserProfile__item1">
                        <span class="justify-start rounded[100%] inline-block flex-row "><img class="rounded-sm h-11" src="../../images/12.jpg"></span>
                        <h5 class="text-base font-bold">Eden Smith</h5>
                        <p class="text-base font-medium">LosAngeles,CA</p>
                        <div class="w-full border-b border-neutral-200 dark:border-neutral-700"></div>
                    </div>
                    <div class="UserProfile__item2">
                        <h5 class="text-base font-bold">My Account</h5>
                        <h5 class="text-base font-bold">My Order</h5>
                        <h5 class="text-base font-bold">Wishlist</h5>
                        <div class="w-full border-b border-neutral-200 dark:border-neutral-700"></div>
                    </div>
                    <div class="UserProfile__item3">
                        <h5 class="text-base font-bold">Dark theme</h5>
                        <h5 class="text-base font-bold">Help</h5>
                        <h5 class="text-base font-bold">Log out</h5>
                        
                    </div>
                </div>

            </div>

        </div>

    </div>
</template>


<style scoped>
/* .UserProfile__items {
    display: flex;
    flex-direction: column; */
    /* padding: 6px; */
    /* gap: 2px;
    align-items: center;
    text-align:justify;
    height: auto;
    width: auto;
    padding: 2rem;
    cursor: pointer;
    margin: 0px 3px;
} */
/* .UserProfile__items .UserProfile__item1__img {
    display: inline-block;
    flex-direction: row;
    justify-content: flex-start;
    border-radius:100%;

} */
</style>