<template>
  <div class="hello1">
    <div class="wrapper">
      <div class="middle-part">
        <div class="card-container">
          <!-- First row of cards -->
          <div class="card">
            <span class="air">Air Quality:</span>
            <span class="card-text">XX</span>
            <span class="good">GOOD</span>
          </div>
          <div class="card">
            <span class="precipitation">Precipitation:</span>
            <span class="card-text">XX</span>
            <div class="card-unit">
              <p>mm</p>
              <p>in</p>
            </div>
          </div>
          <div class="card">
            <span class="wind">Wind:</span>
            <span class="card-text">XX</span>
            <div class="card-unit">
              <p>mph</p>
              <p>kmph</p>
            </div>
          </div>
          <!-- Second row of cards -->
          <div class="card">
            <span class="pressure">Pressure:</span>
            <span class="card-text">XX</span>
            <div class="card-unit">
              <p>mb</p>
              <p>in</p>
            </div>
          </div>
          <div class="card">
            <span class="visibility">Visibility:</span>
            <span class="card-text">XX</span>
            <div class="card-unit">
              <p>km</p>
              <p>mi</p>
            </div>
          </div>
          <div class="card">
            <span class="uv">UV Index:</span>
            <span class="card-text">XX</span>
            <span class="good">GOOD</span>
          </div>
        </div>
      </div>
    <div class="weather-box">
        <div class="weather">
            <h1 class="city-name">Sibiu, Romania</h1>
            <div class="city-temperature">
              <img :src="require('@/style/images/day/113.png')">
              <div class="temperature-info">
                <p class="temperature">20</p>
                <p class="temp-feel">Feels like: </p>
                <div class="feel-like-temp"> 
                    <span>15</span>
                </div>
              </div>
              <div class="unit-container">
                 <p>F</p>
                 <p class="unit">C</p> 
              </div>
              <div class="high-low">
                <p class="high-low-text">H: <span>XX</span></p>
                <p class="high-low-text">L: <span>XX</span></p>
              </div>
            </div>
        </div>
    </div>
    <div class="additional-card-wrapper">
      <div class="additional-card">
        <img :src="require('@/style/images/day/116.png')">
        <h2> March 11th, 2024</h2> 
        <div class="moon-info">
          <div>
            <span class="info-label">Phase:</span>
            <span class="moon-text">Full moon</span>
          </div>
          <div>
            <span class="info-label">Visibility:</span>
            <span class="moon-text">XX%</span>
          </div>
          <div>
            <span class="info-label">Distance:</span>
            <span class="moon-text">XXX,XXX.XX km</span>
          </div>
        </div>
      </div>
    </div>
  </div>
  
 <!-- <div>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul>
    </div>
  -->
  </div>

</template>

<script>

/*import Header from './components/Header.vue' */

export default {
  name: 'HelloWorld'
}
</script>
