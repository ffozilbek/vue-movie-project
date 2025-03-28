<template>
    <div class="section shadow-sm">
        <p class="fs-3 text-uppercase">barcha kinolar soni: {{ allMovieCount }}</p>
        <p class="fs-4 text-uppercase">ko'rilgan kinolar soni: {{ watchedMovieCount }}</p>
    </div>
</template>
<script>
export default {
    props: {
        allMovieCount: {
            type: Number,
            required: true
        },
        watchedMovieCount: {
            type: Array,
            required: true
        }
    }
}
</script>
<style>

</style>