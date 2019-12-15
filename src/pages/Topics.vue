<template>
  <Layout>
    <h1>Topics</h1>
    <ul>
      <li v-for="topics in $page.allTopics.edges" :key="topics.node.id">
        <g-link :to="`/topics/${topics.node.id}`">{{ topics.node.title }}</g-link>
      </li>
    </ul>
  </Layout>
</template>

<page-query>
query getAllTopics {
  allTopics: allContentfulTopics {
    edges {
      node {
        id
        title
        article
        createdAt
        updatedAt
      }
    }
  }
}
</page-query>
