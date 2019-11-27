<template lang="html">
  <div class="">  
<h1>Countries List</h1>
<countries-list :countries='countries'></countries-list>
</div>
</template>

<script>
import {eventBus} from './main.js'
import CountriesList from './components/CountriesList.vue'
import CountryDetail from './components/CountryDetail.vue'

export default {
  name: 'app',
  data(){
    return {
      countries: [],
      selectedCountry: null
    }
  },
  mounted(){
    fetch("https://restcountries.eu/rest/v2/all")
    .then(res => res.json())
    .then(countries => this.countries = countries)
  },
  components: {
    "countries-list": CountriesList,
    "coutry-detail": CountryDetail
  }
}
</script>

<style lang="css" scoped>
</style>
