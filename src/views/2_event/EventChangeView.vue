<template>
  <div>
    <select
      name=""
      id=""
      v-on:change="changeCity($event)"
      v-model="selectedCity"
    >
      <option value="">== Select City ==</option>
      <option
        :value="city.cityCode"
        :key="index"
        v-for="(city, index) in cityList"
      >
        {{ city.title }}
      </option>
    </select>

    <select name="" id="">
      <option
        :value="dong.dongCode"
        :key="index"
        v-for="(dong, index) in selectedDongList"
      >
        {{ dong.dongTitle }}
      </option>
    </select>

    <select name="" id="">
      <option
        :value="dong.dongCode"
        :key="index"
        v-for="(dong, index) in dongList.filter(
          (item) => item.cityCode === selectedCity
        )"
      >
        {{ dong.dongTitle }}
      </option>
    </select>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      selectedCity: '',
      cityList: [
        { title: 'Seoul', cityCode: '02' },
        { title: 'Incheon', cityCode: '032' },
        { title: 'Busan', cityCode: '051' },
        { title: 'Jeju', cityCode: '064' }
      ],
      dongList: [
        { cityCode: '02', dongCode: '1', dongTitle: 'S1동' },
        { cityCode: '02', dongCode: '2', dongTitle: 'S2동' },
        { cityCode: '02', dongCode: '3', dongTitle: 'S3동' },
        { cityCode: '032', dongCode: '1', dongTitle: 'I1동' },
        { cityCode: '032', dongCode: '2', dongTitle: 'I2동' },
        { cityCode: '032', dongCode: '3', dongTitle: 'I3동' },
        { cityCode: '051', dongCode: '1', dongTitle: 'B1동' },
        { cityCode: '051', dongCode: '2', dongTitle: 'B2동' },
        { cityCode: '051', dongCode: '3', dongTitle: 'B3동' },
        { cityCode: '064', dongCode: '1', dongTitle: 'J1동' },
        { cityCode: '064', dongCode: '2', dongTitle: 'J2동' },
        { cityCode: '064', dongCode: '3', dongTitle: 'J3동' }
      ],
      selectedDongList: []
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    changeCity(event) {
      console.log(event)
      this.selectedDongList = this.dongList.filter(
        (dong) => dong.cityCode === this.selectedCity
      )
    }
  }
}
</script>
