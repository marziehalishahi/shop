<script setup>
// import { defineProps } from 'vue';

defineProps([
    'image'
]);
</script>

<template>
    <div>
        <div class="flex justify-between mb-3 shopping_cart__elements">
        <div>
            <img class="object-contain w-[96px] h-[96px] rounded-md" :src="image">
        </div>
        <div class="flex flex-col justify-between flex-1 px-4">
            <div class="flex justify-between flex-1">
                <div class="">
                    <div class="font-bold">Rey Nylon Backpack</div>
                    <div class="flex items-center text-gray-500">
                        <div class="">Natural</div>
                        <span class="h-4 mx-2 text-black border-l border-black"></span>
                        <div class="">xl</div>
                    </div>
                </div>
                <div class="flex items-center h-8 px-3 py-1 font-bold text-green-500 border-2 border-green-500 rounded-md ">
                    $74</div>
            </div>


            <div class="flex items-center justify-between flex-1">
                <div class="text-gray-500 ">Qty <span>1</span></div>
                <div class="font-extrabold text-blue-600">Remove</div>
            </div>


        </div>

    </div>
    </div>

</template>

<style scoped></style>