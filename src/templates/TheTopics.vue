<template>
  <Layout>
    <h1>{{ $page.topics.title }}</h1>
    <main>
      <div v-html="article"></div>
    </main>
  </Layout>
</template>

<page-query>
  query topics($id: ID!) {
    topics: contentfulTopics(id: $id) {
      title
      article
    }
  }
</page-query>

<script>
import markdownIt from 'markdown-it'
export default {
  computed: {
    article() {
      const md = new markdownIt()
      return md.render(this.$page.topics.article)
    }
  }
}
</script>