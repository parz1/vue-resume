<template>
  <div>
    <input
      class="w-4/12 p-4 mt-8 shadow-lg rounded"
      type="text"
      v-model="keyValue"
      placeholder="输入搜索内容"
      @input="onInput"
    />

    <div
      class="p-6 mt-4 text-left max-w-sm mx-auto bg-white rounded-xl shadow-md flex items-center space-x-4"
      v-for="(item, index) in results"
      :key="index"
    >
      <div class="flex-shrink-0">
        <img class="h-12 w-12" src="../assets/logo.png" alt="ChitChat Logo" />
      </div>
      <div>
        <div class="text-xl font-medium text-black">{{ item.title }}</div>
        <p class="text-gray-500">{{ item.content.substring(0, 20)}}</p>
      </div>
    </div>
  </div>
</template>
<script lang="ts">
import { ref } from 'vue'
import articles from './articles.ts'
interface Article {
  title: String,
  content: String,
  cover: String
}
export default {
  data() {
    return {
      keyValue: '',
      results: [],
      articles
    }
  },
  methods: {
    onInput() {
      let self = this
      console.log(self.articles)
      let articles: Array<Article> = self.articles
      self.results = articles.filter((e: Article) => {
        console.log(typeof e.title)
        let flag = 0
        let title = e.title
        let content = e.content
        if (title && content.search(self.keyValue) !== -1)
          flag = 1
        if (content && content.search(self.keyValue) !== -1)
          flag = 1
        return flag === 1
      })
    }
  },
}
</script>
<style>
</style>