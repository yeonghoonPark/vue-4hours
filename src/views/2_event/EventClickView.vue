<template>
  <div>
    <button v-on:click="increaseCnt">Add 1</button>
    <p>{{ cnt }}</p>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      cnt: 0
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    increaseCnt() {
      this.cnt += 1
    }
  }
}
</script>
