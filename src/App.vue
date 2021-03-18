<template>
<!--  <img alt="Vue logo" src="./assets/logo.png" />-->
  <h4>PremiumizeMe Viewer</h4>
  <div class="row">
    <movie-component class="col-xs-12 col-sm-6" v-for="movie in movies" v-bind:movie="movie"></movie-component>
  </div>


</template>

<script>
import MovieComponent from "./components/MovieComponent.vue";
import {Movie} from "./model/Movie";
export default {
  name: 'App',
  components: {
    MovieComponent
  },
  data() {
    let m = new Movie();
    m.id = 1;
    m.title = 'Best Movie';
    m.altTitle = 'vs the world';
    m.description = ' A Movie about love, fights, betrayal and self-esteem';
    m.cover = 'https://upload.wikimedia.org/wikipedia/en/3/39/ScottPilgrim.jpg';
    m.screens = 'https://i0.wp.com/doblu.com/wp-content/uploads/2010/11/scottpilgrim13609.jpg';
    m.tags = ['Action', 'Comedy', 'Romance'];
    console.log('movie');
    console.log(m);
    return {
      movies: [m, m],
    };
  }
}
</script>
