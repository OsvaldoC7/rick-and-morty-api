<template>
  <section>
    <div class="grid grid-cols-3 gap-12 md:px-36 lg:px-52 pb-10">
      <div class="bg-gray-600 rounded-2xl transform duration-300 hover:scale-105" v-for="character in characters" :key="character.id">
        <card-character :character="character"/>
      </div>
    </div>
  </section>
</template>

<script>
import { onMounted, computed } from 'vue'
import { useStore } from 'vuex'
import CardCharacter from './CardCharacater.vue'

export default {
  components: {
    CardCharacter,
  },

  setup() {
    const store = useStore()

    //const characters = computed(() => store.state.charactersFilter)
    const characters = computed(() => store.getters.getCharactersFilter)

    onMounted(() => {
      store.dispatch('getCharacters')
    })

    return {
      characters,
    }

  }
}
</script>

<style>

</style>