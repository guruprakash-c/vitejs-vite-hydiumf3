<script setup> 
import Header from './components/Header.vue';
import Jumbotron from './components/Jumbotron.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';
</script>

<template>
    <Header/>
    <main class="container">
        <Jumbotron/>
        <div class="row g-4 justify-content-start">
        <Main/>
        </div>
    </main>
    <Footer/>  
</template>

<style scoped>

</style>

