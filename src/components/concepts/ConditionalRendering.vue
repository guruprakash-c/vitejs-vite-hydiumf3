<script setup>
import { ref } from 'vue'; 

const number = ref(2);

</script>
<template>
    <article>
        <h1>Conditional Rendering</h1>
        <pre>
            v-if( n % 2 ) 
            v-else-if( n % 3 )
            v-else: 1
            v-show: 1 
            --------------
            v-for: Check Navigation &raquo;
        </pre>
        <input type="number" class="form-control w-25" @change="number = inputValue" v-model="inputValue" min="0" step="1" max="5"/>
        <p v-if="number % 2 == 0">{{ number }} is even </p>
        <p v-else-if="number % 3 == 0">{{ number }} is odd </p>
        <p v-else>{{ number }} is neither even nor odd </p>
        <p v-show="number == 1">{{number}} is natural</p>
    </article>
</template>