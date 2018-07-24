<template>
  <div class="container">
    <h1>Home</h1>
    <form @submit.prevent="submit">
      <input v-model="search" placeholder="Search" autofocus />
    </form>
  </div>
</template>

<script>
export default {
  components: {

  },
  data() {
    return {
      search: ''
    }
  },
  methods: {
    submit(event) {
      this.$router.push('results/' + this.search)
    }
  }
}
</script>

<style scoped>

</style>


