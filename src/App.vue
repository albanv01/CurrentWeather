<template>
  <div id="app">
    <div class="container">
      <h1 class="title container">Current Weather</h1>
      <Weather v-bind:llista-ciutats="Europa"></Weather>
      <Weather v-bind:llista-ciutats="Asia"></Weather>
      <Weather v-bind:llista-ciutats="Africa"></Weather>
      <Weather v-bind:llista-ciutats="America"></Weather>
      <Weather v-bind:llista-ciutats="Oceania"></Weather>

    </div>
  </div>
</template>

<script>
import Weather from "@/components/Weather";

export default {
  name: 'App',
  data: function () {
    return {
      selectedContinente: "Todos",
      toggled: false,
      fechaDia: null,
      fechaMes: null,
      fechaYear: null,
      continentes:[
        "Todos",
        "Europa",
        "Asia",
        "America",
        "Africa",
        "Oceania",
      ],
      Europa: [
        "Barcelona",
        "Lleida",
        "Zaragoza",
        "Sevilla",
        "Madrid",
        "París",
        "Viborg",
        "Londres",
        "Berlin",
      ],
      Asia:[
        "Lahore",
        "Beijing",
        "Kabul",
        "Tehran",
        "Seoul",
        "Tokyo",
        "Shanghai",
      ],
      America:[
        "New York",
        "New Jersey",
        "Toronto",
        "Medellin",
        "Buenos Aire",
      ],
      Africa:[
        "Nairobi",
        "Cairo",
        "Luanda",
        "Acra",
        "Dakar",
      ],
      Oceania:[
        "Sydney",
        "Brisbane",
        "Melbourne",
        "Canberra",
        "Auckland",
      ],
      monthNames: [
        "Enero",
        "Febrero",
        "Marzo",
        "Abril",
        "Mayo",
        "Junio",
        "Julio",
        "Agosto",
        "Septiembre",
        "Octubre",
        "Noviembre",
        "Diciembre"],
    }
  },
  components: {
    Weather
  }
}
</script>

<style>

</style>
