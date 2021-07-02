<template>
  <div>
    <div>
      <h2>Making API request-the vue way</h2>
      <hr>
    </div>

    <div class="container row">
      <Card v-for="post in allPosts" :key="post.id" :post="post" class="ml-auto mr-auto"/>
      <buttn class="btn btn-danger" v-scroll-to="'body'">Back to Top</buttn>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import Card from '@/components/Card.vue'
export default {
  components: {
    Card
  },
  data() {
    return {
      posts: ''
    }
  },
  computed: {
    allPosts() {
      return this.$store.getters.posts
    }
  },
  
  head: {
    title: "List of Posts"
  }
}
</script>


