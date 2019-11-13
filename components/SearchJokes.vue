<template>
  <form @submit.prevent="onSubmit">
    <input v-model="text" type="text" placeholder="Search Jokes..." />
    <input id type="submit" value="Search Jokes" name />
  </form>
</template>

<script>
export default {
  name: 'SearchJokes',
  data() {
    return {
      text: ''
    }
  },
  methods: {
    onSubmit() {
      this.$emit('search-text', this.text)
      this.text = ''
    }
  }
}
</script>

<style scoped></style>
