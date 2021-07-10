<template>
  <div class="nav-bar flex justify-between">
    <div class="logo flex items-center">
      <img src="../assets/logo.png" width="48" class="p-3" alt="">
      <div class="font-bold">Goder.Club</div>
    </div>
    <div class="nav flex items-center font-light">
      <div class="pr-4">首页</div>
      <div class="pr-4">评测</div>
      <div class="pr-4">用户</div>
    </div>
  </div>
</template>
<script lang="ts">
import { ref, defineComponent } from 'vue'
export default {
  data() {
    return {
      tag: ['Home', 'Tech', 'Intro']
    }
  }
}
</script>
<style>
.nav-bar {
  @apply bg-white mb-10 shadow-lg;
  height: 48px;
}
</style>