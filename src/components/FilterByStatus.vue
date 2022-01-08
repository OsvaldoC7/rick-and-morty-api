<template>
  <div class="grid justify-items-center pb-10">
    <div class="bg-gray-600 flex flex-row w-1/4 justify-evenly py-3 rounded-xl text-white font-semibold transform duration-300 hover:scale-105">
      <div class="hover:text-yellow-600 cursor-pointer" @click="filter('')">
        All
      </div>
      <div class="hover:text-yellow-600 cursor-pointer" @click="filter('Alive')">
        Alive
      </div>
      <div class="hover:text-yellow-600 cursor-pointer" @click="filter('Dead')">
        Dead
      </div>
      <div class="hover:text-yellow-600 cursor-pointer" @click="filter('unknown')">
        Unknown
      </div>
    </div>
  </div>
</template>

<script>
import {useStore} from 'vuex'

export default {
  setup() {
    const store = useStore()

    const filter = ((s) => store.dispatch('filterByStatus', s))
    
    return {
      filter,
    }
  }
}
</script>

<style>

</style>