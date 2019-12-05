<template>
  <header class="flex items-center justify-start h-16 border-b">
    <transition name="searchbar-fade">
      <div v-if="!isSearchbarVisible" class="flex items-center justify-start h-full">
        <div class="w-16 h-full">
          <a @click="searchbarVisible()" href="#" class="inline-block relative h-full w-full p-2">
            <svg class="absolute inset-0 m-auto h-4" viewBox="0 0 50 50">
              <rect fill="none" height="50" width="50"/>
              <circle fill="none" cx="21" cy="20" r="16" stroke="#000000" stroke-linecap="round" stroke-miterlimit="10" stroke-width="5"/>
              <line fill="none" stroke="#000000" stroke-miterlimit="10" stroke-width="6" x1="32.229" x2="45.5" y1="32.229" y2="45.5"/>
            </svg>
          </a>
        </div>
        <h1 class="font-extrabold tracking-wider lowercase">Graphix</h1>
      </div>
    </transition>
    <transition name="searchbar-fade"
                v-on:after-enter="searchbarFocus()">
      <div v-if="isSearchbarVisible" class="flex items-center w-full h-full">
        <div class="flex-1 w-full h-full pl-5">
          <input ref="searchbar" class="w-full h-full px-5 outline-none bg-gray-100 uppercase text-sm" placeholder="Search for graphics">
        </div>
        <div class="w-16 h-full bg-gray-900 text-gray-200">
          <button @click="searchbarInvisible()" class="h-full w-full">
            <svg class="h-5 m-auto text-gray-200" viewBox="0 0 24 24">
              <path fill="currentColor" d="M23.954 21.03l-9.184-9.095 9.092-9.174-2.832-2.807-9.09 9.179-9.176-9.088-2.81 2.81 9.186 9.105-9.095 9.184 2.81 2.81 9.112-9.192 9.18 9.1z"/>
            </svg>
          </button>
        </div>
      </div>
    </transition>
  </header>
</template>

<script>
export default {
  name: 'topBar',
  data: function () {
    return {
      isSearchbarVisible: false
    }
  },
  methods: {
    searchbarVisible: function () {
      this.isSearchbarVisible = true;
    },
    searchbarInvisible: function () {
      this.isSearchbarVisible = false;
    },
    searchbarFocus: function () {
      this.$refs.searchbar.focus();
    }
  }
}
</script>

<style scoped>
.searchbar-fade-enter {
  opacity: 0;
}

.searchbar-fade-enter-active {
  transition: all 0.3s ease-in-out;
}

.searchbar-fade-leave-active {
  opacity: 0;
}
</style>