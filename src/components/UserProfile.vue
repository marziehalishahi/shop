<script setup>
    import { ref } from 'vue';
    import { UserIcon } from '@heroicons/vue/24/outline';
    let profile = ref(false)
    function toggle(){
        profile.value = !profile.value
    }

</script>


<template>
    
        <UserIcon @click="toggle" class="w-6 h-6 text-black"></UserIcon>
        <div class="relative">
            <div :class="{'hidden' : !profile}" class="absolute text-white bg-black rounded-sm shadow-md w-36 h-44 top-8">
            safdsf
            </div>
        </div>


</template>


<style scoped>
</style>