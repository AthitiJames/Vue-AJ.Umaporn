<script setup>
  let number = 1 ;
  const color = 'color: green'
  const imagePath = '../public/images/camylla-battani-A5E-ym6WyGM-unsplash.jpg'

</script>

<template>
<h1>Hello, Vue.js</h1>
<h2>V-TEXT</h2>
  <p v-text = "number"></p> 
  <p>{{ number }}</p> <!--shot-->
<br>
<h2>V-BIND</h2>
  <p :style="color">V-bind shot</p>
  <p v-bind:style="color">V-bind</p>
  <img src='./assets/logo.png'>
  <img :src="imagePath" alt="" srcset="">

</template>
 
<style>

</style>

