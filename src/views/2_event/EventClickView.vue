<template>
  <div>
    <button v-on:click="increaseCnt">+ 1</button>
    <button v-on:click="decreaseCnt">- 1</button>
    <p>{{ cnt }}</p>

    <input type="number" v-model="v" />
    <div>{{ v }}</div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      cnt: 0,
      v: 0
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    increaseCnt() {
      this.cnt += 1
    },
    decreaseCnt() {
      this.cnt -= 1
    }
  }
}
</script>
