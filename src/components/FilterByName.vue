<template>
  <div class="grid justify-items-center pb-10">
    <div class="w-1/4 transform duration-300 hover:scale-105">
      <input 
        @keyup="filter()"
        class="rounded-xl py-3 px-3 w-full"
        id="" 
        name="" 
        placeholder="Search by name"
        type="text" 
        v-model="name"
      >
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
import { useStore } from 'vuex'

export default {
  setup() {
    const store = useStore()
    const name = ref('')

    const filter = () => {
      store.dispatch('filterByName', name.value)
    }

    return {
      name,
      filter,
    }
  }
}
</script>

<style>

</style>