<template>
  <Searchbar/>
  <Slider :title="'All movies'" :link="'https://api-workshop-laravel.herokuapp.com/api/movies?page=3'">
  </Slider>
  <Slider :title="'All series'" :link="'https://api-workshop-laravel.herokuapp.com/api/series?page=3'">
  </Slider>  
  <Slider :title="'Best ranked'" :link="'https://api-workshop-laravel.herokuapp.com/api/movies?page=1'">
  </Slider>
</template>

<script setup>
  import Searchbar from '../components/Searchbar.vue';
  import Slider from '../components/Slider.vue';
</script>