<template>
  <div>
    <div>
      <select name="" id="">
        <option value=""></option>
        <option
          v-bind:value="city.code"
          v-bind:key="city.code"
          v-for="city in cities"
        >
          {{ city.title }}
        </option>
      </select>

      <!-- v-for를 사용할 땐 항상 key가 필요하다. -->
      <ul>
        <li v-bind:key="변수명아무거나.code" v-for="변수명아무거나 in cities">
          {{ 변수명아무거나.title }}
        </li>
      </ul>
      <hr />

      <div>
        <table>
          <thead>
            <tr>
              <th>Product-Number</th>
              <th>Product-Name</th>
              <th>Price</th>
              <th>OrderQuantity</th>
              <th>Total</th>
            </tr>
          </thead>
          <tbody>
            <!-- v-for에서는 map이나 forEach와 같이 3가지의 argument를 받을 수 있는 것으로 추정 -->
            <tr v-bind:key="index" v-for="(item, index) in drinkList">
              <td>{{ item.drinkId }}</td>
              <td>{{ item.drinkName }}</td>
              <td>{{ item.price }}</td>
              <td><input type="number" v-model="item.qty" /></td>
              <td>{{ item.qty * item.price }}</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      cities: [
        { title: 'Seoul', code: '02' },
        { title: 'Busan', code: '051' },
        { title: 'Jeju', code: '064' }
      ],
      drinkList: [
        {
          drinkId: '1',
          drinkName: 'Coke',
          price: 700,
          qty: 0
        },
        {
          drinkId: '2',
          drinkName: 'Fanta',
          price: 500,
          qty: 0
        },
        {
          drinkId: '3',
          drinkName: 'Sprite',
          price: 900,
          qty: 0
        },
        {
          drinkId: '4',
          drinkName: 'Pepsi',
          price: 650,
          qty: 0
        },
        {
          drinkId: '5',
          drinkName: 'Milkiss',
          price: 300,
          qty: 0
        },
        {
          drinkId: '6',
          drinkName: '815',
          price: 8500,
          qty: 0
        },
        {
          drinkId: '7',
          drinkName: 'Cass',
          price: 800,
          qty: 0
        }
      ]
    }
  }
}
</script>

<style scoped>
table {
  margin: 0 auto;
}
</style>
