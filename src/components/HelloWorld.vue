<template>
  <div class="hello1">
    <div class="wrapper">
      <div class="middle-part">
        <div class="card-container">
          <!-- First row of cards -->
          <div class="card">
            <span class="air">Air Quality:</span>
            <div class="air-text">
              <span class="card-text">XX</span>
            </div>
            <div class="air-cond">
              <span class="good">GOOD</span>
            </div>
          </div>
          <div class="card">
            <span class="precipitation">Precipitation:</span>
            <div class="precip-text">
              <span class="card-text" id="precip-value">XX</span>
            </div>
            <div class="card-unit">
              <button class="unit-button1" data-unit="mm">mm</button>
              <button class="unit-button2" data-unit="in">in</button>
            </div>
          </div>
          <div class="card">
            <span class="wind">Wind:</span>
            <span class="wind-text">XX</span>
            <div class="card-unit">
              <button class="wind-button" data-unit="mph">mph</button>
              <button class="wind-button" data-unit="kmph">kmph</button>
            </div>
          </div>
          <!-- Second row of cards -->
          <div class="card">
            <span class="pressure">Pressure:</span>
            <div class="press-text">
              <span class="card-text">XX</span>
            </div>
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
            <div class="uv-text">
              <span class="card-text">XX</span>
            </div>
            <span class="good">GOOD</span>
          </div>
        </div>
      </div>
    <div class="weather-box">
        <div class="weather">
            <h1 class="city-name">Sibiu, Romania</h1>
            <div class="city-temperature">
              <img :src="require('@/style/images/night/113.png')" class="weather-icon">
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
                <p class="high-low-text">H: <span class="high">XX</span></p>
                <p class="high-low-text">L: <span class="low">XX</span></p>
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
  
  </div>

</template>

<script>

export default {
  name: 'HelloWorld'
}
</script>
