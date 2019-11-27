<template lang="html">
  <select>
    <option disabled value="">Select a Country</option>
    <list-item v-for="(country,index) in countries" :country='country' :key='index'></list-item>
  </select>
<!-- <ul>
  <list-item v-for="(country,index) in countries" :country='country' :key='index'></list-item>
</ul> -->
</template>


<!-- <select v-model="selectedOperation">
      <option disabled value="">Select an Operation</option>
      <option v-for="operation in operations">{{operation}}</option>
    </select>
-->
<script>
import ListItem from './ListItem.vue'

export default {
  name: 'countries-list',
  props: ['countries'],
  components: {
    "list-item": ListItem
  }

}
</script>

<style lang="css" scoped>
</style>
