<script setup>
import { ref } from 'vue'; 
const pages = ref([
  {
    title: 'Components',
    url: '/Components',
    target: '_top',
    className: 'blog-nav-item'
  },
  {
    title: 'Renders',
    url: '/renders',
    target: '_top',
    className: 'blog-nav-item'
  },
  {
    title: 'Hooks',
    url: '/hooks',
    target: '_top',
    className: 'blog-nav-item'
  },
  {
    title: 'Support',
    url: 'https://vuejs.org',
    target: '_blank',
    className: 'blog-nav-item'
  }
]);
</script>
<template>
<header>
  <div class="container">
    <nav class="blog-nav">
      <a class="blog-nav-item active" href="/">
        <img src="/src/assets/vue.svg" width="25" class="align-middle me-1"/>VueJS
      </a>
      <a :class="className" v-for="({title, url, target, className},i) in pages" :key="i" :href="url" :target="target">{{title}}</a>
    </nav>
  </div>
</header>
</template>
<style>
header {
  background-color: #428bca;
  -webkit-box-shadow: inset 0 -2px 5px rgba(0, 0, 0, .1);
  box-shadow: inset 0 -2px 5px rgba(0, 0, 0, .1);
}

/* Nav links */
.blog-nav-item {
  position: relative;
  display: inline-block;
  padding: 10px;
  font-weight: 500;
  color: #cdddeb !important;
  text-decoration: none
}
.blog-nav-item:hover,
.blog-nav-item:focus {
  color: #fff !important;
  text-decoration: none;
}

/* Active state gets a caret at the bottom */
.blog-nav .active {
  color: #fff;
  text-decoration: none;
}
.blog-nav .active:after {
  position: absolute;
  bottom: 0;
  left: 50%;
  width: 0;
  height: 0;
  margin-left: -5px;
  vertical-align: middle;
  content: " ";
  border-right: 5px solid transparent;
  border-bottom: 5px solid;
  border-left: 5px solid transparent;
}
</style>