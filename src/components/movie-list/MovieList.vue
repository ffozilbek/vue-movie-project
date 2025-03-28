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
    props: {
        movies: {
            type: Array,
            required: true
        },

    }
}
</script>
<style>

</style>