<template>
 <!-- <img alt="Vue logo" src="./assets/logo.png">``--> 
 <!-- <HeaderComponent></HeaderComponent> --> 

 <nav class="nav"> 
    <div class="icons"> 
      <img ref="navIcon" class="nav-icon" :src="require('@/style/images/nav.svg')" alt="Navigation" @click="toggleSearchHistory">
      <div ref="searchHistory" class="search-history" v-show="showSearchHistory">
        <!-- Search history content goes here -->
      </div>
      <button @click="handleSearch">
        <img class="search-icon" :src="require('@/style/images/search.svg')" alt="Search">
      </button>
      <input type="text" class="search-input" placeholder="City name..." ref="searchInput">
    </div>
  </nav>
  
  <!--- <HelloWorld></HelloWorld> -->

  <div class="hello1">
    <div class="wrapper">
      <div class="middle-part">
        <div class="card-container">
          <!-- First row of cards -->
          <div class="card">
            <span class="air">Air Quality:</span>
            <div class="air-text">
              <span class="card-text" ref="airText">XX</span>
            </div>
            <div class="air-cond" ref="airCond">
              <span class="good">GOOD</span>
            </div>
          </div>
          <div class="card">
            <span class="precipitation">Precipitation:</span>
            <div class="precip-text">
              <span class="card-text" id="precip-value" ref="precipValue">XX</span>
            </div>
            <div class="card-unit">
              <button class="unit-button1" data-unit="mm" @click="handleUnitButtonClick('mm')" ref="precip1">mm</button>
              <button class="unit-button2" data-unit="in" @click="handleUnitButtonClick('in')" ref="precip2">in</button>
            </div>
          </div>
          <div class="card">
            <span class="wind">Wind:</span>
            <div class="wind-text">
              <span class="card-text" id="wind-value" ref="windValue">XX</span>
            </div>
            <div class="card-unit">
              <button class="unit-button1" data-unit="mph" @click="handleUnitButtonClick('mph')" ref="wind1">mph</button>
              <button class="unit-button2" data-unit="kmph" @click="handleUnitButtonClick('kmph')" ref="wind2">kmph</button>
            </div>
          </div>
          <!-- Second row of cards -->
          <div class="card">
            <span class="pressure">Pressure:</span>
            <div class="press-text">
              <span class="card-text" id="press-value" ref="pressValue">XX</span>
            </div>
            <div class="card-unit">
              <button class="unit-button1" data-unit="mb" @click="handleUnitButtonClick('mb')" ref="press1">mb</button>
              <button class="unit-button2" data-unit="inc" @click="handleUnitButtonClick('inc')" ref="press2">in</button>
            </div>
          </div>
          <div class="card">
            <span class="visibility">Visibility:</span>
            <div class="vis-text">
              <span class="card-text" id="vis-value" ref="visValue">XX</span>
            </div>
            <div class="card-unit">
              <button class="unit-button1" data-unit="km" @click="handleUnitButtonClick('km')" ref="vis1">km</button>
              <button class="unit-button2" data-unit="mi" @click="handleUnitButtonClick('mi')" ref="vis2">mi</button>
            </div>
          </div>
          <div class="card">
            <span class="uv">UV Index:</span>
            <div class="uv-text">
              <span class="card-text" ref="uvText">XX</span>
            </div>
            <span class="good">GOOD</span>
          </div>
        </div>
      </div>
      <div class="weather-box">
        <div class="weather">
          <h1 class="city-name" ref="cityName">Sibiu, Romania</h1>
          <div class="city-temperature">
            <img :src="require('@/style/images/night/113.png')" class="weather-icon" ref="weatherIcon">
            <div class="temperature-info">
              <p class="temperature" ref="temperature">20</p>
              <p class="temp-feel">Feels like: </p>
              <div class="feel-like-temp" ref="feelLike">
                <span>15</span>
              </div>
            </div>
            <div class="unit-container">
              <button class="unit-button1" data-unit="F" @click="handleUnitButtonClick('F')" ref="Far">F</button>
              <button class="unit-button2" data-unit="C" @click="handleUnitButtonClick('C')" ref="Cel">C</button>
            </div>
            <div class="high-low">
              <p class="high-low-text">H: <span class="high" ref="high">XX</span></p>
              <p class="high-low-text">L: <span class="low" ref="low">XX</span></p>
            </div>
          </div>
        </div>
      </div>
      <div class="additional-card-wrapper">
        <div class="additional-card">
          <img :src="require('@/style/images/day/116.png')" ref="additionalCardImage">
          <h2 ref="dateInfo"> March 11th, 2024</h2>
          <div class="moon-info">
            <div>
              <span class="info-label">Phase:</span>
              <span class="moon-text" ref="moonPhase">Full moon</span>
            </div>
            <div>
              <span class="info-label">Visibility:</span>
              <span class="moon-text" ref="moonVisibility">XX%</span>
            </div>
            <div>
              <span class="info-label">Distance:</span>
              <span class="moon-text" ref="moonDistance">XXX,XXX.XX km</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="next-days">
  <h2>5-day forecast</h2>
  <div class="days-container">
    <div class="day-card">
      <span class="day" ref="day1">Monday</span>
      <img :src="require('@/style/images/night/113.png')" ref="day1Icon">
      <div class="min-max">
        <p class="max-min-text">H: <span ref="max1">XX</span></p>
        <p class="max-min-text">L: <span ref="min1">XX</span></p>
      </div>
      <span class="card-text" ref="prog1">Mostly sunny</span>
    </div>
    <div class="day-card">
      <span class="day" ref="day2">Tuesday</span>
      <img ref="day2Icon">
      <div class="min-max">
        <p class="max-min-text">H: <span ref="max2">XX</span></p>
        <p class="max-min-text">L: <span ref="min2">XX</span></p>
      </div>
      <span class="card-text" ref="prog2">Mostly sunny</span>
    </div>
    <div class="day-card">
      <span class="day" ref="day3">Wednesday</span>
      <img ref="day3Icon">
      <div class="min-max">
        <p class="max-min-text">H: <span ref="max3">XX</span></p>
        <p class="max-min-text">L: <span ref="min3">XX</span></p>
      </div>
      <span class="card-text" ref="prog3">Mostly sunny</span>
    </div>
    <div class="day-card">
      <span class="day" ref="day4">Thursday</span>
      <img ref="day4Icon">
      <div class="min-max">
        <p class="max-min-text">H: <span ref="max4">XX</span></p>
        <p class="max-min-text">L: <span ref="min4">XX</span></p>
      </div>
      <span class="card-text" ref="prog4">Mostly sunny</span>
    </div>
    <div class="day-card">
      <span class="day" ref="day5">Friday</span>
      <img ref="day5Icon">
      <div class="min-max">
        <p class="max-min-text">H: <span ref="max5">XX</span></p>
        <p class="max-min-text">L: <span ref="min5">XX</span></p>
      </div>
      <span class="card-text" ref="prog5">Mostly sunny</span>
    </div>
  </div>
</div>
<div class="last-week">
    <h2>Last 7 days</h2>
    <div class="days-container">
        <div class="day-card">
            <span class="day" ref="lastday0">Sunday</span>
            <img class="nav-icon" :src="require('@/style/images/night/113.png')" ref="lastIcon0">
            <div class="min-max">
                <p>H: <span ref="lasthigh0"></span></p>
                <p>L: <span ref="lastlow0"></span></p>
            </div>
            <span class="card-text" ref="lastprog0">Mostly sunny</span>
        </div>
        <div class="day-card">
            <span class="day" ref="lastday1">Monday</span>
            <img class="nav-icon" :src="require('@/style/images/night/113.png')" ref="lastIcon1">
            <div class="min-max">
                <p>H: <span ref="lasthigh1"></span></p>
                <p>L: <span ref="lastlow1"></span></p>
            </div>
            <span class="card-text" ref="lastprog1">Mostly sunny</span>
        </div>
        <div class="day-card">
            <span class="day" ref="lastday2">Tuesday</span>
            <img class="nav-icon" :src="require('@/style/images/night/113.png')" ref="lastIcon2">
            <div class="min-max">
                <p>H: <span ref="lasthigh2"></span></p>
                <p>L: <span ref="lastlow2"></span></p>
            </div>
            <span class="card-text" ref="lastprog2">Mostly sunny</span>
        </div>
        <div class="day-card">
            <span class="day" ref="lastday3">Wednesday</span>
            <img class="nav-icon" :src="require('@/style/images/night/113.png')" ref="lastIcon3">
            <div class="min-max">
                <p>H: <span ref="lasthigh3"></span></p>
                <p>L: <span ref="lastlow3"></span></p>
            </div>
            <span class="card-text" ref="lastprog3">Mostly sunny</span>
        </div>
        <div class="day-card">
            <span class="day" ref="lastday4">Thursday</span>
            <img class="nav-icon" :src="require('@/style/images/night/113.png')" ref="lastIcon4">
            <div class="min-max">
                <p>H: <span ref="lasthigh4"></span></p>
                <p>L: <span ref="lastlow4"></span></p>
            </div>
            <span class="card-text" ref="lastprog4">Mostly sunny</span>
        </div>
        <div class="day-card">
            <span class="day" ref="lastday5">Friday</span>
            <img class="nav-icon" :src="require('@/style/images/night/113.png')" ref="lastIcon5">
            <div class="min-max">
                <p>H: <span ref="lasthigh5"></span></p>
                <p>L: <span ref="lastlow5"></span></p>
            </div>
            <span class="card-text" ref="lastprog5">Mostly sunny</span>
        </div>
        <div class="day-card">
            <span class="day" ref="lastday6">Saturday</span>
            <img class="nav-icon" :src="require('@/style/images/night/113.png')" ref="lastIcon6">
            <div class="min-max">
                <p>H: <span ref="lasthigh6"></span></p>
                <p>L: <span ref="lastlow6"></span></p>
            </div>
            <span class="card-text" ref="lastprog6">Mostly sunny</span>
        </div>
    </div>
</div>

  <!-- <PredComp msg="Weather App soon"/> -->
</template>

<script>
/*
document.addEventListener("DOMContentLoaded", function() {
  const searchBox = document.querySelector(".search-input");
  const searchBtn = document.querySelector(".search-icon");

  function handleSearch(event) {
    if (event.key === "Enter" || event.type === "click") {
      checkWeather(searchBox.value);
      searchBox.value = ''; // Empty the input field after search
    }
  }

  searchBtn.addEventListener("click", handleSearch);
  searchBox.addEventListener("keypress", handleSearch);
}); */

export default {
  data() {
    return {
      showSearchHistory: false,
      cityName: '' // Initialize cityName data property
    }
  },
  mounted() {
    this.$refs.searchInput.focus(); // Focus the input field when the component is mounted

    const searchBox = this.$refs.searchInput;
    searchBox.addEventListener("keypress", (event) => {
      if (event.key === "Enter") {
        this.cityName = event.target.value.trim();
        this.handleSearch();
        console.log(this.cityName)
        //this.$refs.searchInput.value = '';
      }
    });
  },
  methods: {
    toggleSearchHistory() {
      this.showSearchHistory = !this.showSearchHistory;
    },
    async checkWeather(cityName) {
      const apiKey = "f63c3c4f5a0646b783d94446241303";
      const apiUrl = "http://api.weatherapi.com/v1/forecast.json?&days=7&aqi=yes&q=";

      const response = await fetch(`${apiUrl}&q=${cityName}&key=${apiKey}`);
      const data = await response.json();

      if (data.error) {
        console.error("Error fetching weather data:", data.error.message);
        return;
      }

      const airQualityIndex = data.current.air_quality['us-epa-index'];
      const airQualityText = this.getAirQualityText(airQualityIndex);
      this.$refs.airCond.textContent = airQualityText;
      this.$refs.airText.textContent = data.current.air_quality['us-epa-index'];
      this.$refs.uvText.textContent = data.current.uv;

      const sunsetTime = new Date(data.forecast.forecastday[0].astro.sunset);
      const sunriseTime = new Date(data.forecast.forecastday[0].astro.sunrise);
      const currentTime = new Date();
      console.log('Current Time:', currentTime);
      const isDayTime = currentTime > sunriseTime && currentTime < sunsetTime;
      console.log('Is Day Time:', isDayTime);
      console.log('currentTime:', currentTime);
      console.log('sunriseTime:', data.forecast.forecastday[0].astro.sunrise);
      console.log('sunsetTime:', data.forecast.forecastday[0].astro.sunset);
      console.log('currentTime > sunriseTime:', currentTime > sunriseTime);
      console.log('currentTime < sunsetTime:', currentTime < sunsetTime);
      let iconPath = data.current.condition.icon;
      if (!isDayTime) {
          iconPath = iconPath.replace('/day/', '/night/');
      }
      console.log('Adjusted Icon Path:', iconPath);
      // Set the image source
      console.log('Weather Icon Ref Element:', this.$refs.weatherIcon); // Check if this is the correct reference
      this.$refs.weatherIcon.src = `https:${iconPath}`;
      this.$refs.weatherIcon.onload = () => {
        // Image loaded successfully
        console.log('Weather icon loaded successfully');
      };
      this.$refs.weatherIcon.onerror = () => {
        // Error loading image
        console.error('Error loading weather icon');
      };
      
      this.$refs.cityName.textContent = `${data.location.name}, ${data.location.country}`;
      this.$refs.temperature.textContent = data.current.temp_c;
      this.$refs.feelLike.textContent = data.current.feelslike_c;
      this.$refs.high.textContent = data.forecast.forecastday[0].day.maxtemp_c;
      this.$refs.low.textContent = data.forecast.forecastday[0].day.mintemp_c;

      const currentDate = new Date();
      const options = { month: 'long', day: 'numeric', year: 'numeric' };
      const formattedDate = currentDate.toLocaleDateString('en-US', options);
      this.$refs.dateInfo.textContent = formattedDate;
      this.$refs.moonPhase.textContent = data.forecast.forecastday[0].astro.moon_phase;

      const daysOfWeek = ['Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday'];
      const dayIndex = currentDate.getDay(); // 0 for Sunday, 1 for Monday, etc.
      this.$refs.day1.textContent = daysOfWeek[dayIndex];
      const image1Url = `https:${data.forecast.forecastday[1].day.condition.icon}`;
      this.$refs.day1Icon.src = image1Url;
      this.$refs.max1.textContent = data.forecast.forecastday[1].day.maxtemp_c;
      this.$refs.min1.textContent = data.forecast.forecastday[1].day.mintemp_c;
      this.$refs.prog1.textContent = data.forecast.forecastday[1].day.condition.text;

      this.$refs.day2.textContent = daysOfWeek[dayIndex+1];
      const image2Url = `https:${data.forecast.forecastday[2].day.condition.icon}`;
      this.$refs.day2Icon.src = image2Url;
      this.$refs.max2.textContent = data.forecast.forecastday[2].day.maxtemp_c;
      this.$refs.min2.textContent = data.forecast.forecastday[2].day.mintemp_c;
      this.$refs.prog2.textContent = data.forecast.forecastday[2].day.condition.text;

      this.$refs.day3.textContent = daysOfWeek[dayIndex+2];
      const image3Url = `https:${data.forecast.forecastday[3].day.condition.icon}`;
      this.$refs.day3Icon.src = image3Url;
      this.$refs.max3.textContent = data.forecast.forecastday[3].day.maxtemp_c;
      this.$refs.min3.textContent = data.forecast.forecastday[3].day.mintemp_c;
      this.$refs.prog3.textContent = data.forecast.forecastday[3].day.condition.text;

      this.$refs.day4.textContent = daysOfWeek[(dayIndex + 3) % 7];
      const image4Url = `https:${data.forecast.forecastday[4].day.condition.icon}`;
      this.$refs.day4Icon.src = image4Url;
      this.$refs.max4.textContent = data.forecast.forecastday[4].day.maxtemp_c;
      this.$refs.min4.textContent = data.forecast.forecastday[4].day.mintemp_c;
      this.$refs.prog4.textContent = data.forecast.forecastday[4].day.condition.text;

      this.$refs.day5.textContent = daysOfWeek[(dayIndex + 4) % 7];
      const image5Url = `https:${data.forecast.forecastday[5].day.condition.icon}`;
      this.$refs.day5Icon.src = image5Url;
      this.$refs.max5.textContent = data.forecast.forecastday[5].day.maxtemp_c;
      this.$refs.min5.textContent = data.forecast.forecastday[5].day.mintemp_c;
      this.$refs.prog5.textContent = data.forecast.forecastday[5].day.condition.text;
      this.fetchLast7DaysWeather(cityName)

    },
   async fetchLast7DaysWeather(city) {
    const apiKey = "f63c3c4f5a0646b783d94446241303";
    const apiUrl = `http://api.weatherapi.com/v1/history.json?key=${apiKey}&q=${city}&dt=2024-03-13&end_dt=2024-02-19`;
    console.log(apiUrl, 'log');
    
    const response = await fetch(`${apiUrl}`);
    const data = await response.json();
    console.log(response)
    console.log('API Response:', data);
    console.error('NOO', city);

    // this.$refs.lastday0.textContent = data.current.temp_c;
    
  },
    handleSearch() {
      if (this.cityName.trim()) {
        this.checkWeather(this.cityName);
        this.updateSearchHistory(this.cityName);
        //this.cityName = ''; // Empty the input field after search
      }
    },
    getAirQualityText(index) {
      switch (index) {
        case 1:
          return "Good";
        case 2:
          return "Moderate";
        case 3:
          return "Unhealthy";
        case 4:
          return "Unhealthy";
        case 5:
          return "Very unhealthy";
        case 6:
          return "Hazardous";
        default:
          return "Unknown";
      }
    },
    async handleUnitButtonClick(unit) {
      const cityName = this.$refs.searchInput.value.trim(); // Assuming you have a search input ref
      if (!cityName) {
        console.error('City name is required.');
        return;
      }

      const apiKey = "f63c3c4f5a0646b783d94446241303";
      const apiUrl = "http://api.weatherapi.com/v1/forecast.json?&days=7&aqi=yes&q=";
      
      try {
        const response = await fetch(`${apiUrl}&q=${cityName}&key=${apiKey}`);
        const data = await response.json();

        if (data.error) {
          console.error('Error fetching data:', data.error.message);
          return;
        }

        const precipValueElement = this.$refs.precipValue;
        const windValueElement = this.$refs.windValue;
        const pressValueElement = this.$refs.pressValue;
        const visValueElement = this.$refs.visValue;
        const tempValueElement = this.$refs.temperature;
        const feelValueElement = this.$refs.feelLike;
        const highValueElement = this.$refs.high;
        const lowValueElement = this.$refs.low;

        const high1 = this.$refs.max1;
        const low1 = this.$refs.min1;
        const high2 = this.$refs.max2;
        const low2 = this.$refs.min2;
        const high3 = this.$refs.max3;
        const low3 = this.$refs.min3;
        const high4 = this.$refs.max4;
        const low4 = this.$refs.min4;
        const high5 = this.$refs.max5;
        const low5 = this.$refs.min5;
        if (unit === 'mm') {
          precipValueElement.textContent = data.current.precip_mm;
        } else if (unit === 'in') {
          precipValueElement.textContent = data.current.precip_in;
        } else if (unit === 'mph') {
          windValueElement.textContent = data.current.wind_mph;
        }
        else if (unit === 'kmph') {
          windValueElement.textContent = data.current.wind_kph;
        }
        else if (unit === 'mb') {
          pressValueElement.textContent = data.current.pressure_mb;
        }
        else if (unit === 'inc') {
          pressValueElement.textContent = data.current.pressure_in;
        }
        else if (unit === 'km') {
          visValueElement.textContent = data.current.vis_km;
        }
        else if (unit === 'mi') {
          visValueElement.textContent = data.current.vis_miles;
        }
        else if (unit === 'F') {
          tempValueElement.textContent = data.current.temp_f;
          feelValueElement.textContent = data.current.feelslike_f;
          highValueElement.textContent = data.forecast.forecastday[0].day.maxtemp_f;
          lowValueElement.textContent = data.forecast.forecastday[0].day.mintemp_f;

          high1.textContent = data.forecast.forecastday[1].day.maxtemp_f;
          low1.textContent = data.forecast.forecastday[1].day.mintemp_f;
          high2.textContent = data.forecast.forecastday[2].day.maxtemp_f;
          low2.textContent = data.forecast.forecastday[2].day.mintemp_f;
          high3.textContent = data.forecast.forecastday[3].day.maxtemp_f;
          low3.textContent = data.forecast.forecastday[3].day.mintemp_f;
          high4.textContent = data.forecast.forecastday[4].day.maxtemp_f;
          low4.textContent = data.forecast.forecastday[4].day.mintemp_f;
          high5.textContent = data.forecast.forecastday[5].day.maxtemp_f;
          low5.textContent = data.forecast.forecastday[5].day.mintemp_f;
        }
        else if (unit === 'C') {
          tempValueElement.textContent = data.current.temp_c;
          feelValueElement.textContent = data.current.feelslike_c;
          highValueElement.textContent = data.forecast.forecastday[0].day.maxtemp_c;
          lowValueElement.textContent = data.forecast.forecastday[0].day.mintemp_c;

          high1.textContent = data.forecast.forecastday[1].day.maxtemp_c;
          low1.textContent = data.forecast.forecastday[1].day.mintemp_c;
          high2.textContent = data.forecast.forecastday[2].day.maxtemp_c;
          low2.textContent = data.forecast.forecastday[2].day.mintemp_c;
          high3.textContent = data.forecast.forecastday[3].day.maxtemp_c;
          low3.textContent = data.forecast.forecastday[3].day.mintemp_c;
          high4.textContent = data.forecast.forecastday[4].day.maxtemp_c;
          low4.textContent = data.forecast.forecastday[4].day.mintemp_c;
          high5.textContent = data.forecast.forecastday[5].day.maxtemp_c;
          low5.textContent = data.forecast.forecastday[5].day.mintemp_c;
        }
         else {
          console.error('Invalid unit:', unit);
        }
      } catch (error) {
        console.error('Error fetching data:', error);
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
      const historyList = document.querySelector('.search-history');
      if (historyList) {
        historyList.innerHTML = ''; // Clear the existing content
        if (searchHistory && searchHistory.length > 0) {
          searchHistory.forEach(city => {
            const listItem = document.createElement('li');
            listItem.textContent = city;
            historyList.appendChild(listItem);
          });
        } else {
          const noHistoryItem = document.createElement('li');
          noHistoryItem.textContent = 'No search history available';
          historyList.appendChild(noHistoryItem);
        }
      } else {
        console.error('Search history container not found in the DOM');
      }
    }
  },

  name: 'App'
}
</script>

<style lang="scss">
// empty
</style>
