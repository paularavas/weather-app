<template>
     <nav class="nav"> 
    <div class="icons"> 
      <img class="nav-icon" :src="require('@/style/images/nav.svg')" alt="Navigation">
      <button @click="handleSearch">
        <img class="search-icon" :src="require('@/style/images/search.svg')" alt="Search">
      </button>
      <input type="text" class="search-input" placeholder="City name..." ref="searchInput">
    </div>
  </nav> 
</template>

<script>
export default {
mounted() {
    this.$refs.searchInput.focus(); // Focus the input field when the component is mounted
  },
  methods: {
    handleSearch() {
      const cityName = this.$refs.searchInput.value.trim();
      if (cityName) {
        this.checkWeather(cityName);
        this.updateSearchHistory(cityName);
        this.$refs.searchInput.value = ''; // Empty the input field after search
      }
    },
    updateSearchHistory(cityName) {
      let searchHistory = JSON.parse(localStorage.getItem('searchHistory')) || [];
      searchHistory.unshift(cityName);
      searchHistory = searchHistory.slice(0, 5);
      localStorage.setItem('searchHistory', JSON.stringify(searchHistory));
      this.updateSearchHistoryUI(searchHistory);
    },
    updateSearchHistoryUI(searchHistory) {
      const searchHistoryList = document.querySelector('.search-history');
      searchHistoryList.innerHTML = '';
      searchHistory.forEach(city => {
        const listItem = document.createElement('li');
        listItem.textContent = city;
        searchHistoryList.appendChild(listItem);
      });
    }
  },
  name: 'HeaderComponent'
}; 

</script>