<template>
  <div class="container">
    <post v-for="post in posts" :key="post.id" :post="post"></post>
  </div>
</template>

<script>
  import axios from 'axios'
  import Post from '@/components/Post'

  export default {
    data () {
      return {
        posts: []
      }
    },

    layout: 'posts', 

    head: {
      title: 'Posts'
    },

    components: {
      Post
    },

    // mounted () {
    //     axios.get('https://jsonplaceholder.typicode.com/posts')
    //       .then((response) => {
    //            this.posts = response.data
    //        });
    // }

    async asyncData () {
      // return axios.get('https://jsonplaceholder.typicode.com/posts').then((response) => {
      //   return {
      //     posts: response.data
      //   }
      // })

      let response = await axios.get('https://jsonplaceholder.typicode.com/posts')

      return {
        posts: response.data
      }
    }

  }
</script>
