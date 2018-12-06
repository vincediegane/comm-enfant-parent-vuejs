<template>
  <div>
    <citizen-form ref="formcitizen"></citizen-form>
    <button type="submit" v-on:click="onClick">CLICK</button>
    <hr>
    <citizens ref="citizens" v-on:selected="setSelectedCitizen($event)"></citizens>
    <hr>
    <citizen :citizen="selectedCitizen"></citizen>
  </div>
</template>

<script>
import Citizens from "./Citizens"
import CitizenForm from "./CitizenForm"
import Citizen from "./Citizen"

export default {
  components: {
    Citizens,
    CitizenForm,
    Citizen
  },
  data(){
    return {
      selectedCitizen: {}
    }
  },
  methods: {

    setSelectedCitizen(selectedCitizen){
      this.selectedCitizen = selectedCitizen
    },

    onClick(){
      var all_citizens = this.$refs['citizens'].citizens
      var citizen = this.$refs['formcitizen'].citizen
      all_citizens.push(citizen)
    }
  }
}
</script>

<style>

</style>
