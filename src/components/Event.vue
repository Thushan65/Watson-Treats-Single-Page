<script setup>
import { ref } from "vue";
    const props = defineProps({
        event:{
            type: Object,
            required:true,
        },
    });

    const getImageUrl = (imagePath) => {
    // Assuming your public directory is served at the root
    return import.meta.env.BASE_URL + 'images/' + imagePath;
};

let expand = ref(false);
function showDetails(){
    document.getElementById(`${props.event.id}`).show();
}
function hideDetails(){
    document.getElementById(`${props.event.id}`).close()
}
</script>

<template>
    <div id="events">
        <h2>{{ event.title }}</h2>
        <img :src="getImageUrl(event.image)" alt="Picture of a cake" height="400" width="400">
        <br>
        <button @click="showDetails">View Details</button>
    </div>

    <dialog :id="event.id">
        <div id="dialog">
            <h2>{{ event.title }}</h2>
            <img :src="getImageUrl(event.image)" alt="Picture of a cake" height="400" width="400">
            <p>{{ event.description }}</p>
            <br>
            <button @click="hideDetails">Go Back</button>
        </div>
    </dialog>
</template>


<style lang="scss" scoped>

$font-main: Merriweather, Helvetica, sans-serif;

$font-highlight: 'Bree Serif', Helvetica, sans-serif;

$offwhite: #EEE8D6;

$darkblue: #022933;

$colour-text: $darkblue;

$colour-backgrounds: $offwhite;

@mixin customBorder ($width: 5px, $color: $darkblue, $style: solid) {
border: {
width: $width;
color: $color;
style: $style;
}

}

#events{
font-family:$font-highlight;
background-color:$colour-backgrounds;
color:$colour-text;
text-align: center;
padding-bottom: 2%;
@include customBorder;
h2{
    text-align: center;
}
p{
    text-align: center;
    font-size: x-large;
    background-color:orange;
}
}

button {
  padding: 10px;
  background-color: #ff7e67;
  color: rgb(15, 15, 15);
  text-align: center;
  font-weight: bold;
  display: block;
  width: 98%;
  margin: 0.5em 0 0 0;
  margin-left: 5px;
}

#dialog{
::backdrop {
  background-image: linear-gradient(
    45deg,
    rgb(161, 155, 161),
    rgb(211, 193, 230),
    rgb(155, 182, 210),
    rgb(208, 241, 208)
  );
  opacity: 0.75;
}

img {
  width: 100%;
  height: auto;
  max-width:25rem;
  text-align: center;
  margin-left: 550px;
}

h2,
p {
  width: 90%;
  padding: 0;
  margin: 5px auto;
  text-align: center;
}
}
</style>