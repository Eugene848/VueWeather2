<template>
    <div id="WindComponent" class="wind">
        <img src="../img/wind.png"> {{wind}} <small>м/с</small>
      </div>
</template>

<script>
export default{
  name: 'HumidityComponent',
  props: ['wind'],
  data(){}
}
</script>

<style>

.wind {
  font-family: 'Arial', sans-serif;
  font-size: 40px;
  font-weight: 400;
  color: #fff;
  position: relative;
  display: inline-block;
  line-height: 0.9;
  text-shadow: 2px 2px 2px #444;
  margin: 15px;
}

.wind img {
  width: 30px;
  margin-right: -5px;
  vertical-align: middle;
}

</style>