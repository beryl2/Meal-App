<template>
    <div class="flex flex-col p-8 items-center justify-center">
        <div>
            <input type="text" class="rounded border-2 border-gray-200 w-full" placeholder="Search the meal"/>
        </div>
        

        <div class="flex gap-1">
            <route-link to="/" v-for="letter of letters">
                {{ letters }}
            </route-link>
        </div>
    </div>

</template>

<script setup>
import { computed } from 'vue';
import store from '../store';

const meals= computed(() => store.state.meals);
const  letters= 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'.split('')
</script>

