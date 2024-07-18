<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div id="navigation">
      <nav>
        <RouterLink to="/" style="margin-right: 1%;">Home</RouterLink>
        <RouterLink to="/cakes" style="margin-right: 1%;">Our Cakes</RouterLink>
        <RouterLink to="/events">Our Events</RouterLink>
      </nav>
    </div>
  </header>
  <RouterView/>
</template>


<style lang="scss" scoped>

$font-main: Merriweather, Helvetica, sans-serif;

$offwhite: #EEE8D6;

$colour-backgrounds: $offwhite;
;

#navigation {
font-family:$font-main;
background-color:$colour-backgrounds;
color:black;
text-align: right;
justify-content:space-between;
}

#navigation nav{
  margin-right: 1%;
}
</style>
