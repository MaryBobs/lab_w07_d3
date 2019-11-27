<template lang="html">
  <option v-on:change='handleChange'>{{country.name}}</option>
  <!-- <li v-on:click='handleClick'>{{country.name}}</li> -->
</template>

<script>
import {eventBus} from "../main.js"

export default {
  name: 'list-item',
  props: ['country'],
  methods: {
    handleChange() {
      eventBus.$emit('country-selected', this.country)
    }
  }
}
</script>

<style lang="css" scoped>
</style>
