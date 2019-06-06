<template>
  <section class="slug">
    <h1 class="slug_title">
      タイトル
    </h1>
    <p class="slug_date">2019/5/29</p>
    <vue-markdown>
      # 記事内容
      本文本文本文本文本文本文本文本文本文本文本文本文
    </vue-markdown>
  </section>
</template>

<script>
import VueMarkdown from 'vue-markdown'
export default {
  transition: 'slide-left',
  components: {
     VueMarkdown
  }
}
</script>>

<style scoped>
.slug {
  max-width: 800px;
  margin: 0 auto;
}
.slug_title {
  font-size: 2rem;
  font-weight: bolder;
}
.slug_date {
  font-size: 1rem;
  color: rgb(57, 72, 85);
  text-align: right;
}
</style>
