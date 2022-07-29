<template>
  <div>
    <h1>Hello {{ userName }}</h1>
    <p>{{ message }} {{ userName }} 😀</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userName: 'John Doe',
      message: 'Welcome to the Real World..',
      arr: [],
      obj: {}
    }
  }
}
</script>

<style scoped>
h1 {
  color: #ff0000;
}
</style>
