<template>
  <div class="hello1">
    <div class="wrapper">
      <div class="middle-part">
        <div class="card-container">
          <!-- First row of cards -->
          <div class="card">Air Quality<span class="card-text">XX</span></div>
          <div class="card">Precipitation</div>
          <div class="card">Wind</div>
          <!-- Second row of cards -->
          <div class="card">Pressure</div>
          <div class="card">Visibility</div>
          <div class="card">UV Index</div>
        </div>
      </div>
    <div class="weather-box">
      <div class="box">
        <div class="info">
          <div class="weather">
            <h1 class="city-name">Sibiu, Romania</h1>
            <div class="city-temperature">
              <img :src="require('@/style/images/day/116.png')">
              <div>
                
              </div>
              <p class="temperature">20<span>C</span></p>
              <p class="temp-feel">Feels like:</p>
              <span>15C</span>
              <p class="high-low">H: <span>XX</span></p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div>
      <div class="additional-card">Additional Card</div>
    </div>
  </div>
  <h1>{{ msg }}</h1>
  
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
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>
