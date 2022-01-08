<template>
  <div class="bg-gray-800 min-h-screen">
    <h2 class="text-center font-bold text-2xl text-white py-10">
      Rick And Morty
    </h2>
    <filter-by-name />
    <filter-by-status />
    <list-characters />
  </div>
</template>

<script>
import ListCharacters from './components/ListCharacters.vue'
import FilterByStatus from './components/FilterByStatus.vue'
import FilterByName from './components/FilterByName.vue'

export default {  
  name: 'App',
  components: {
    ListCharacters,
    FilterByStatus,
    FilterByName,
  }
}
</script>

<style>

</style>