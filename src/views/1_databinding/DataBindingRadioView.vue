<template>
  <div>
    <div>
      <input
        type="radio"
        name=""
        id="html"
        value="HTML"
        v-model="favoriteLang"
      />
      <label for="html">HTML</label>
      <input type="radio" name="" id="css" value="CSS" v-model="favoriteLang" />
      <label for="css">CSS</label>
      <input type="radio" name="" id="js" value="JS" v-model="favoriteLang" />
      <label for="js">jabaScript</label>
    </div>
    <div>선택한 지역: {{ favoriteLang }}</div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      favoriteLang: ''
    }
  }
}
</script>
