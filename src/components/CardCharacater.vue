<template>
  <div class="text-white hover:text-yellow-600">
    <img 
      class="rounded-t-2xl"
      :src="character.image" 
      :alt="character.name"
    />
    <div class="p-6">
      <h3 class="font-semibold">
        {{ character.name }}
      </h3>
      <div class="text-gray-400">
        <span :class="
          character.status == 'Alive' ? 'text-green-600' :
          character.status == 'Dead' ? 'text-red-600' : 'text-gray-700'"
          class="text-xl font-black"
        >• </span>
        <span>{{ character.status }} - {{ character.species }}</span>
      </div>
      <div class="text-gray-300">
        <span>Origin: {{ character.origin.name }}</span>
      </div>
      <div class="text-gray-300">
        <span>Location: {{ character.location.name }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['character']
}
</script>

<style>

</style>