<template>
  <div class="card">
    <figure class="figure"><img class="cover" v-bind:src="movie.cover"></figure>
    <div class="card-body">
      <div class="card-title" v-text="movie.title"></div>
      <div class="card-text sub-title" v-text="movie.altTitle"></div>
      <div class="card-text description" v-text="movie.description"></div>

      <div class="tags">
        <div  v-for="tag in movie.tags" class="badge bg-success tag" v-text="tag"></div>
      </div>
    </div>
  </div>
</template>

<script>
import {Movie} from "../model/Movie";

export default {
  name: "MovieComponent",
  props: {
    movie: Movie
  },
}
</script>

<style scoped>

</style>