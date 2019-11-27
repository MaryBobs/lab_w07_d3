<template lang="html">
  <div v-if="country" class="">
    <h3>{{country.name}}</h3>
    <p>{{country.capital}}</p>
    <img :src= 'country.flag' alt="">
  </div>
</template>

<script>

export default {
  name:'country-detail',
  props: ['country']
}
</script>

<style lang="css" scoped>
</style>
