<template>
  <div class="container">
    <div class="row">
      <div class="col-md-8">
        <nuxt></nuxt>
      </div>

      <div class="col-md-4">
        <no-ssr>
          <v-select v-model="selected" placeholder="select category" :options="['foo','bar']"></v-select>
        </no-ssr>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        selected: null
      }
    }
  }
</script>
