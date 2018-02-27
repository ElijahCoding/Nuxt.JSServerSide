<template>
  <div>
    <template v-if="error.statusCode === 404">
      <h1>404</h1>
      <p>That page could not found</p>
    </template>
  </div>
</template>

<script>
  export default {
    props: ['error']
  }
</script>
