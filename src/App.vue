<template>
    <div class="informer-container">
    <TemperatureComponent v-bind:real="real" v-bind:feel="feel"></TemperatureComponent>
    <div class="flex-break"></div>
    <HumidityComponent v-bind:humidity="humidity"></HumidityComponent>
    <div class="vertical-divider"></div>
    <WindComponent v-bind:wind="wind"></WindComponent>
    </div>
</template>

<script>
import TemperatureComponent from './components/TemperatureComponent.vue'
import HumidityComponent from './components/HumidityComponent.vue'
import WindComponent from './components/WindComponent.vue'

export default{
  name: 'app',
  components: {
    TemperatureComponent, 
    HumidityComponent,
    WindComponent
  },
  data(){
  return {
    real: 1,
    feel: '-3.2',
    humidity: 6,
    wind: 20
  }
}
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
#app {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background: rgb(244, 123, 186);
  background: linear-gradient(-25deg, rgba(244, 123, 186, 0.5) 20%, rgba(90, 95, 245, 0.5) 80%);
}

.informer-container {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 400px;
  padding: 30px;
  background-image: url('img/forest.png');
  background-size: cover;
  background-position: center center;
  border-radius: 20px;
  box-shadow: 0px 0px 10px 0px rgba(50, 50, 50, 0.75);
}

.flex-break{
  flex-basis: 100%;
  height: 0;
}

.vertical-divider{
  height: 70px;
  width: 1px;
  background-color: #fff;
  vertical-align: middle;
  display: table-cell;
}

</style>