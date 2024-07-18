<script setup>
import TheCakes from '../components/Cakes.vue'
import Cakes from '/Cakes.json'
import Thefotter from '../components/footer.vue'
</script>

<template>
  <div id="cakes">
    <h1>Our Cakes</h1>
    <div id="cakeeach">
      <TheCakes v-for="(ourcakes, index) in Cakes.cakeslist":key="index":ourcakes="ourcakes"/>
    </div>
    <br>
  </div>
    <Thefotter/>
</template>


<style lang="scss" scoped>

$font-main: Merriweather, Helvetica, sans-serif;

$font-highlight: 'Bree Serif', Helvetica, sans-serif;

$offwhite: #EEE8D6;

$darkblue: #022933;

$orange: #F39856;

$red: #D14348;

$purple: #6D73C2;

$colour-text: $darkblue;

$colour-backgrounds: $offwhite;

@mixin customBorder ($width: 5px, $color: $darkblue, $style: solid) {

border: {

width: $width;

color: $color;

style: $style;

}

}

#cakes{
  background-color: #EEE8D6;

  h1{
    text-align: center;
    color: #022933;
    font-size: 250%;
  }

}

#cakeeach {

font-family:$font-highlight;
background-color:$colour-backgrounds;
color:$colour-text;

display: grid;
grid-template-columns:repeat(2,minmax(100px, 1fr));

font-family: "Courier New";

@include customBorder;

}


</style>