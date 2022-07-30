<template>
  <div>
    <!-- readonly를 사용하여 유저가 값을 바꾸지 못하고 읽을 수 있게만 하는것이 목적이면
    양방향 바인딩인 v-model을 쓸 필요가 없다, 이런 경우에 value라는 속성 값에 직접 v-bind:를
    적용하면 단방향 바인딩의 기능을 수행한다. -->
    <input type="text" name="" id="" v-bind:value="userId" readonly />
    <hr />
    <!-- 속성에 바인딩을 할 때 v-bind: 를 사용하는데 축약형으로 v-bind를 생략하고 :로 사용가능. -->
    <input type="text" name="" id="" :value="userId" readonly />
    <hr />
    <img :src="imgSrc" alt="cat" style="width: 200px; height: auto" />
    <br />
    <form action="">
      <input type="search" name="" id="" v-model="txt1" required />
      <button :disabled="txt1 === ''">check</button>
    </form>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      userId: 'Cat from the street',
      imgSrc:
        'https://upload.wikimedia.org/wikipedia/commons/thumb/4/4d/Cat_November_2010-1a.jpg/1200px-Cat_November_2010-1a.jpg',
      txt1: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
