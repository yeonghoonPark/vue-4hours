<template>
  <div>
    <form>
      <input type="text" v-model="userId" placeholder="plz press any key" />
      <button v-on:click="handleClick1">Click1</button>
      <button @click="handleClick2">Click2</button>
      <button @click="chageData">Change Data</button>
    </form>
    <div>input창의 value = {{ userId }}</div>
    <hr />
    <input type="text" v-model="num1" /> +
    <input type="text" v-model="num2" /> =
    <span>{{ parseInt(num1) + parseInt(num2) }}</span>
    <hr />
    <input type="text" v-model.number="num3" /> +
    <input type="text" v-model.number="num4" /> =
    <span>{{ num3 + num4 }}</span>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      userId: '',
      num1: 0,
      num2: 0,
      num3: 0,
      num4: 0
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    handleClick1(event) {
      event.preventDefault()
      console.log('Is it working?')
    },
    handleClick2(event) {
      event.preventDefault()
      console.log(`Is it working too?! ${this.userId}!?`)
    },
    chageData(event) {
      event.preventDefault()
      this.userId = "userId's changed"
      console.log(this.userId)
    }
  }
}
</script>
