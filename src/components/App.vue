<template>
  <div class="App">
    <AppInfo :allMovieCount="movies.length" :watchedMovieCount="movies.filter(m=>m.watched).length"/>
    <div class="section shadow-sm">
        <SearchPanel />
        <Filter />
    </div>
    <MovieList :movies="movies"/>
    <MovieAddForm @createMovie="createMovie"/>
  </div>
</template>

<script>
import AppInfo from "@/components/app-info/AppInfo.vue";
import SearchPanel from "@/components/search-panel/SearchPanel.vue";
import Filter from "@/components/filter/Filter.vue";
import MovieList from "@/components/movie-list/MovieList.vue";
import MovieAddForm from "@/components/movie-add-form/MovieAddForm.vue";

export default {
  components: {
    AppInfo,SearchPanel,Filter,MovieList,MovieAddForm
  },
  data() {
        return {
            movies: [
            {
                name: "Spiderman",
                viewers: 856,
                checked: true,
                watched: false,
                liked: false,
                id: 1,
            },
            {
                name: "Game of Thrones",
                viewers: 1235,
                checked: false,
                watched: true,
                liked: false,
                id: 2,
            },
            {
                name: "Avengers Doomsday",
                viewers: 4789,
                checked: false,
                watched: false,
                liked: true,
                id: 3,
            }
            ]
        }
    },
    methods: {
      createMovie(item) {
        this.movies.push(item)

      }
    }
};
</script>
<style>
.App {
    max-width: 900px;
    width: 100%;
    margin-left: auto;
    margin-right: auto;
    padding: 50px 30px;
    font-family: monospace;
}

.section {
    background-color: #fefee5;
    padding: 15px;
}

.section:not(:last-child) {
    margin-bottom: 15px;
}

</style>
