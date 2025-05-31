<script setup>
import { ref } from 'vue';
debugger;
let count = ref(0);
</script>

<template>
    <article>
        <h1>ref()</h1>
        <pre>
           count:  {{ count }}
        </pre>
        <div class="btn-group">
            <button class="btn btn-primary" @click="count++">[+]</button>
            <button class="btn btn-danger" @click="count--">[-]</button>
        </div>
    </article>
</template>