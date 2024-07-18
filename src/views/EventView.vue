<script setup>
import TheEvents from '../components/Getevents.vue';
import Thefotter from '../components/footer.vue';
</script>
<template>
    <div id="event">
      <h1>Our Events</h1>
      <div id="eachevent">
        <TheEvents myFile="https://github.com/Thushan65/WD_Assignment/blob/main/Events.json"/>
      </div>
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

#event{
  background-color: #EEE8D6;

  h1{
    text-align: center;
    color: #022933;
    font-size: 250%;
  }

}

#eachevent {
font-family:$font-highlight;
background-color:$colour-backgrounds;
color:$colour-text;

@include customBorder;
}
</style>