<template>
  <content class="p-6 pb-10 m-6  w-8/12 mx-auto bg-white rounded-xs shadow-md block">
    <h1 class="block text-6xl font-semibold">{{ msg }}</h1>
    <div class="flex flex-row justify-between">
      <div>
        <h2>Information FrontEnd Engineer</h2>
        <div class="flex flex-row flex-wrap text-left">
          <div v-for="(item, index) in info" :key="index" class="w-6/12 pr-4">
            <span class="font-bold block">{{item.tag}}</span>
            {{item.value}}
          </div>
        </div>
      </div>
      
      <img alt="Goder logo" src="../assets/logo.png" />
    </div>
    <h2>Project Experience</h2>
    <div class="text-left">
      <div class="font-bold block">2017~2021 Zhejiang Ansuw Tech Company</div>
      <div>Experience in project management refers to time spent planning, leading, directing, and managing projects. For example, some typical responsibilities of a project manager include:</div>
      <div>
        <div>
          <span class="font-bold px-4 mt-4"> · Planing</span>
          Project managers create a blueprint that will guide the entire project from ideation to fruition, clarifying its scope, necessary resources, anticipated timeframe, communication strategy, and more.
        </div>
        <div>
          <span class="font-bold px-4 mt-4"> · Leading</span>
          Project managers lead the project team through the process, meaning they have excellent communication and people skills.
        </div>
        <div>
          <span class="font-bold px-4 mt-4"> · Execution</span>
          A project manager is likely to engage in the tangible activities required for moving the project forward.
        </div>
      </div>
    </div>
  </content>
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue'
export default defineComponent({
  name: 'Resume',
  props: {
    msg: {
      type: String,
      required: true
    }
  },
  setup: () => {
    const count = ref(0)
    const info = [
      {
        tag: 'Phone',
        value: '18267952768'
      },
      {
        tag: 'Blog',
        value: 'https://parz1.goder.club'
      },
      {
        tag: 'Mail',
        value: 'parz1zhou@gmail.com'
      },
      {
        tag: 'Address',
        value: '(Empty)'
      },
      {
        tag: 'Occupation',
        value: 'Front-end engineer'
      },
    ]
    return { count, info }
  }
})
</script>

<style scoped>
h1 {
  @apply my-8 text-6xl text-left font-bold;
}
h2 {
  @apply my-8 block text-xl text-left font-semibold;
}
</style>
