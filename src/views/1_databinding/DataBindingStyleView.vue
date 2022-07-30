<template>
  <div>
    <div style="color: red; font-size: 30px">
      Style Binding: color=red, font-size=30px
    </div>
    <div v-bind:style="style1">Style Binding: color=green, font-size=30px</div>
    <button v-on:click="onColorChange">Color Change Blue</button>
    <button @click="style1.color = 'yellow'">Color Change Yellow</button>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      style1: {
        color: 'green',
        fontSize: '30px'
      }
    }
  },
  methods: {
    onColorChange() {
      this.style1.color = 'blue'
    }
  }
}
</script>

<style></style>
