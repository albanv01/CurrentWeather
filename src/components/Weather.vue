<template>
  <section class="pb-3">
    <div class="row pl-2">
      <div class="col-6">
        <select class="form-control" v-model="selectedCity">
          <option v-for="ciutat in llistaCiutats" v-bind:key="ciutat">{{ciutat}}</option>
        </select>
      </div>
    </div>
    <WeatherNow v-bind:ciudad-selecionada=selectedCity></WeatherNow>
  </section>
</template>

<script>
import WeatherNow from "@/components/WeatherNow";

export default {
  name: "InfoMeteo",
  props: {
    llistaCiutats: Array,
    continentes: Array,
  },
  data(){
    return {
      selectedCity: this.llistaCiutats[0]
    }
  },
  mounted: function (){
    return{
      selectedCity:this.llistaCiutats[0]
    }
  },
  components: {
    WeatherNow,

  }
}
</script>

<style scoped>

</style>