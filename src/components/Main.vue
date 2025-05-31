<script setup>
import Sidebar from './Sidebar.vue';
import MyReactiveComponents from './concepts/MyReactiveComponents.vue'
</script>
<template>
    <main class="col-lg-8 col-md-8 col-xs-12  col-sm-12">
        <MyReactiveComponents/>
    </main>
    <Sidebar/>
</template>
<style>
article {
  background: #fff;
  padding: 2rem;

}
</style>