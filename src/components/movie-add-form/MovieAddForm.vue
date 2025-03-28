<template>
    <div class="section shaow">
        <h3 class="mb-3">Yangi kino qo'shish</h3>
        <form @submit.prevent>
            <div class="input-group d-flex justify-content-center mb-3">
                <input class="form-control me-2" type="text" placeholder="Kino nomi" :value="name" @input="name = $event.target.value">
                <input class="form-control" type="number" placeholder="Nechi marta ko'rilgan" :value="viewers" @input="viewers=$event.target.value">
            </div>
            <button class="btn btn-dark d-block w-50 mx-auto" type="submit" @click="addMovies">Qo'shish</button>
        </form>
    </div>
</template>
<script>
export default {
    data() {
        return {
            name: "",
            viewers: ""
        }
    },
    methods: {
        addMovies() {
            const newMovies = {
                name: this.name,
                viewers: this.viewers,
                liked: false,
                watched: false,
                checked: false,
                id: Date.now()

            }
            this.$emit("createMovie", newMovies)
            this.name=""
            this.viewers=""
        }


    }
}
</script>
<style></style>