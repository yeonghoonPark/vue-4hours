<template>
  <div>
    <div v-bind:class="{ 'text-red': hasError, active: isActive }">
      Class Binding1
    </div>
    <div v-bind:class="class2">Class Binding2</div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      isActive: false,
      hasError: false,
      class2: ['active', 'text-red']
    }
  }
}
</script>

<style scoped>
.active {
  background: greenyellow;
  font-weight: bold;
}

.text-red {
  color: red;
}
</style>
