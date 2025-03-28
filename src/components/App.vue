<template>
  <div class="App">
    <AppInfo />
    <div class="section shadow-sm">
        <SearchPanel />
        <Filter />
    </div>
    <MovieList />
    <MovieAddForm />
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
