<template>
  <div>
    <select v-model="selectCity">
      <option value=""></option>
      <option value="02">Seoul</option>
      <option value="051">Busan</option>
      <option value="064">Jeju</option>
    </select>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      selectCity: '02'
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
