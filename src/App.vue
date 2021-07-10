<template>
  <NavBar />
  <div class="flex flex-col justify-center items-center">
    <img src="./assets/logo.png" width="80" height="80" alt="">
    <div class="text-5xl pt-4">Goder</div>
    <div class="text-sm">游戏人的攻略归宿</div>
  </div>
  <Search />
  <!-- <Resume msg="parz1's Resume" /> -->
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Resume from './components/Resume.vue'
import Search from './components/Search.vue'
import './index.css'
import NavBar from './components/NavBar.vue'

export default defineComponent({
  name: 'App',
  components: {
    Resume,
    Search,
    NavBar
  }
})
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
