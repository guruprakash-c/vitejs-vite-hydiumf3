<script setup>
import { ref, computed } from 'vue';
const number = ref(1);
const squaredNumber = computed(() => number.value * number.value);
</script>
<template>
    <article>
        <h1>Computed Properties </h1>
        <pre>
        Original number: {{ number }}
        Squared number: {{ squaredNumber }}
        </pre>
        <input type="number" class="form-control w-25" @change="number = inputValue" v-model="inputValue" min="0" step="2" max="10"/>
    </article>
</template>