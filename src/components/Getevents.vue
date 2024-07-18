<script setup>
import { ref, onMounted } from "vue";
import EventItem from "./Event.vue";

    const myProps = defineProps({
        myFile:{
            type: String,
            required:true
        }
    })

    let myJson = ref([]);
    onMounted(() =>{
        fetchData();
    })

    /*function fetchData() {
        fetch(myProps.myFile)
        .then((stream) => stream.json())
        .then((data) => (myJson.value = data))
        .catch((error) => console.error(error));
    }*/

    function fetchData() {
    fetch(`https://raw.githubusercontent.com/Thushan65/WD_Assignment/main/Events.json`)
    .then(response => {
        if (!response.ok) {
            throw new Error('Failed to fetch data from GitHub.');
        }
        return response.json();
    })
    .then(data => {
        myJson.value = data;
    })
    .catch(error => console.error(error));
}


</script>

<template>
    <div id="event2">
        <div id="eventeach">
        <EventItem v-for="(event, index) in myJson.events":key="index":event="event"></EventItem>
        </div>
    </div>
</template>



<style lang="scss" scoped>

$font-main: Merriweather, Helvetica, sans-serif;

$font-highlight: 'Bree Serif', Helvetica, sans-serif;

$offwhite: #EEE8D6;

$darkblue: #022933;

$colour-text: $darkblue;

$colour-backgrounds: $offwhite;

#event2{
  background-color: #EEE8D6;

  h1{
    text-align: center;
    color: #022933;
    font-size: 250%;
  }

}

#eventeach {

font-family:$font-highlight;
background-color:$colour-backgrounds;
color:$colour-text;

display: grid;
grid-template-columns:repeat(3,minmax(100px, 1fr));
}
</style>