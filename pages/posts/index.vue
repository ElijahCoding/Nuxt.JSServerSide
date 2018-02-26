<template>
  <p>{{ posts }}</p>
</template>

<script>
  import axios from 'axios'

  export default {
    data () {
      return {
        posts: []
      }
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
