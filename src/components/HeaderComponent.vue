<template>
     <nav class="nav"> 
      <div class="icons"> 
        <img class="nav-icon" :src="require('@/style/images/nav.svg')" alt="Navigation">
        <button @click="toggleSearch">
          <img class="search-icon" :src="require('@/style/images/search.svg')" alt="Search">
          </button>
          <input v-if="showSearch" type="text" class="search-input" placeholder="City name..." @click.stop>
      </div>
    </nav>  
</template>

<script>
export default {
  data() {
    return {
      showSearch: false // Initially hide the search bar
    };
  },
  methods: {
    toggleSearch() {
      this.showSearch = !this.showSearch; // Toggle the visibility of the search bar
    }
  },
  name: 'HeaderComponent'
} 
</script>