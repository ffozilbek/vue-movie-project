<template>
    <div class="section shadow-sm">
        <ul class="list-group">
            <MovieListItem v-for="movie in movies" :movie="movie"/>
        </ul>
    </div>
</template>
<script>
import MovieListItem from '@/components/movie-list-item/MovieListItem.vue';

export default {
    components: {
        MovieListItem
    },
    data() {
        return {
            movies: [
            {
                name: "Spiderman",
                viewers: 856,
                checked: true,
                watched: false,
                liked: false
            },
            {
                name: "Game of Thrones",
                viewers: 1235,
                checked: false,
                watched: true,
                liked: false
            },
            {
                name: "Avengers Doomsday",
                viewers: 4789,
                checked: false,
                watched: false,
                liked: true
            }
            ]
        }
    }
}
</script>
<style>

</style>