<script setup>
import { RouterLink, RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue'
import FooterComp from './components/FooterComp.vue'


const logo_src = "/img/logo.png";
const app_name = "/img/logo.png";

</script>

<template>
  <NavBar :logo=logo_src :alt=app_name />
  <RouterView />
  <FooterComp />
</template>

<style>
* {
  font-family: Helvetica;
  padding: 0;
  margin: 0;
  box-sizing: border-box;

}

.main-container {
  margin: 50px;
  min-height: 250px;
}

h1 {
  text-align: center;
  font-style: 42px;
  margin-bottom: 30px;
  color: #222;
  font-weight: 700;

}
</style>