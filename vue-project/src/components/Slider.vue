<template>
    <div class="category">
        <h2>{{ title }}</h2>
        <a href="./pages/allmovies.html" class="allbutton" alt="Voir tout"
        >See all</a>
    </div>
    <div class="cards slides" aria-label="carrousel 5 slides" tabindex="0">
        <Carte v-for="i in 5"></Carte>
    </div>
</template>

<script setup>
    import Carte from './Carte.vue';
    import axios from "axios";
    import { ref } from "vue"
    const element = ref ([])
    const props = defineProps({
        title:{
            type: String,
            required: true
        }
    })

    async function getMovies(){
        const response = await axios.get(props.link)
        if (typeof response.data.movies != 'undefined')
        {element.value = response.data.movies}
        else
        element.value = response.data.series;
    }
    getMovies();
</script>