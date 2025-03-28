<template>
    <li class="list-group-item d-flex align-items-center justify-content-between">
        {{ movie.name }}
        <div>
            <span class="me-4">{{ movie.viewers }}</span>
            <div class="btn-group">
                <button class="btn btn-outline-dark"><i class="fa-solid fa-check"></i></button>
                <button class="btn btn-outline-dark"><i class="fa-solid fa-heart"></i></button>
                <button class="btn btn-outline-dark"><i class="fa-solid fa-eye"></i></button>
            </div>
        </div>
    </li>
</template>
<script>
export default {
    props: {
        movie: {
            type: Object,
            required: true
        }
    }
}
</script>
<style>

</style>