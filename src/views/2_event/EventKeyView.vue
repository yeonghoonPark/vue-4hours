<template>
  <div>
    <input
      type="search"
      name=""
      id=""
      v-model="searchText"
      @keyup="checkEnter($event)"
    />

    <input
      type="search"
      name=""
      id=""
      v-model="searchText"
      @keyup.enter="doSearch"
    />

    <button @click="doSearch">Search</button>
    <button type="submit" @click.prevent="doSearch">Submit</button>
  </div>
</template>

<script>
// .enter
// .tab
// .delete
// .esc
// .space
// .up
// .down
// .left
// .right
// .stop = event.stopPropagation()
// .prevent = event.preventDefault()
export default {
  components: {},
  data() {
    return {
      searchText: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    doSearch() {
      console.log(this.searchText)
    },
    checkEnter(event) {
      if (event.keyCode === 13) {
        this.doSearch()
        this.searchText = ''
      }
    }
  }
}
</script>
