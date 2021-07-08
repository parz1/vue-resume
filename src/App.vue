<template>
  <Resume msg="parz1's Resume" />
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Resume from './components/Resume.vue'
import './index.css'

export default defineComponent({
  name: 'App',
  components: {
    Resume
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
  margin-top: 60px;
}
</style>
