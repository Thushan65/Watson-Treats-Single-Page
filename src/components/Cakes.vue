<script setup>
defineProps({
    ourcakes:{
        type: Object,
        required: true
    }
})


const getImageUrl = (imagePath) => {
    // Assuming your public directory is served at the root
    return import.meta.env.BASE_URL + 'images/' + imagePath;
};
</script>

<template>
    <div id="eachcake">
        <div>
            <h2>{{ ourcakes.name }}</h2>
            <img :src="getImageUrl(ourcakes.image)" alt="Picture of a cake" height="400" width="400">
            <p>£ {{ ourcakes.price }}</p>
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

@mixin customBorder ($width: 5px, $color: $darkblue, $style: solid) {
border: {
width: $width;
color: $color;
style: $style;
}

}

#eachcake {
font-family:$font-highlight;
background-color:$colour-backgrounds;
color:$colour-text;
text-align: center;
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
</style>
