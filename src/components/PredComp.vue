<template>
   <!-- <img class="nav-icon" :src="require('@/style/images/night/113.png')"> --> 
    <div class="next-days">
        <h2>5-day forecast</h2>
        <div class="days-container">
            <div class="day-card">
                <span class="day">Monday</span>
                <img class="nav-icon" :src="require('@/style/images/night/113.png')">
                <div class="min-max">
                    <p>H: </p>
                    <p>L: </p>
                </div>
                <span class="card-text">Mostly sunny</span>
        </div>
            <div class="day-card">
                <span class="day">Tuesday</span>
                <img class="nav-icon" :src="require('@/style/images/night/113.png')">
                <div class="min-max">
                    <p>H: </p>
                    <p>L: </p>
                </div>
                <span class="card-text">Mostly sunny</span>
            </div>
            <div class="day-card">
                <span class="day">Wednesday</span>
                <img class="nav-icon" :src="require('@/style/images/night/113.png')">
                <div class="min-max">
                    <p>H: </p>
                    <p>L: </p>
                </div>
                <span class="card-text">Mostly sunny</span>
            </div>
            <div class="day-card">
                <span class="day">Thursday</span>
                <img class="nav-icon" :src="require('@/style/images/night/113.png')">
                <div class="min-max">
                    <p>H: </p>
                    <p>L: </p>
                </div>
                <span class="card-text">Mostly sunny</span>
            </div>
            <div class="day-card">
                <span class="day">Friday</span>
                <img class="nav-icon" :src="require('@/style/images/night/113.png')">
                <div class="min-max">
                    <p>H: </p>
                    <p>L: </p>
                </div>
                <span class="card-text">Mostly sunny</span>
            </div>
        </div>
    </div>
    <div class="last-week">
        <h2>last 7 days</h2>
        <div class="days-container">
            <div class="day-card">
                <span class="day">Sunday</span>
                <img class="nav-icon" :src="require('@/style/images/night/113.png')">
                <div class="min-max">
                    <p>H: </p>
                    <p>L: </p>
                </div>
                <span class="card-text">Mostly sunny</span>
        </div>
            <div class="day-card">
                <span class="day">Monday</span>
                <img class="nav-icon" :src="require('@/style/images/night/113.png')">
                <div class="min-max">
                    <p>H: </p>
                    <p>L: </p>
                </div>
                <span class="card-text">Mostly sunny</span>
            </div>
            <div class="day-card">
                <span class="day">Tuesday</span>
                <img class="nav-icon" :src="require('@/style/images/night/113.png')">
                <div class="min-max">
                    <p>H: </p>
                    <p>L: </p>
                </div>
                <span class="card-text">Mostly sunny</span>
            </div>
            <div class="day-card">
                <span class="day">Wednesday</span>
                <img class="nav-icon" :src="require('@/style/images/night/113.png')">
                <div class="min-max">
                    <p>H: </p>
                    <p>L: </p>
                </div>
                <span class="card-text">Mostly sunny</span>
            </div>
            <div class="day-card">
                <span class="day">Thursday</span>
                <img class="nav-icon" :src="require('@/style/images/night/113.png')">
                <div class="min-max">
                    <p>H: </p>
                    <p>L: </p>
                </div>
                <span class="card-text">Mostly sunny</span>
            </div>
            <div class="day-card">
                <span class="day">Friday</span>
                <img class="nav-icon" :src="require('@/style/images/night/113.png')">
                <div class="min-max">
                    <p>H: </p>
                    <p>L: </p>
                </div>
                <span class="card-text">Mostly sunny</span>
            </div>
            <div class="day-card">
                <span class="day">Saturday</span>
                <img class="nav-icon" :src="require('@/style/images/night/113.png')">
                <div class="min-max">
                    <p>H: </p>
                    <p>L: </p>
                </div>
                <span class="card-text">Mostly sunny</span>
            </div>
        </div>
    </div>
    <h1>{{ msg }}</h1>
</template>

<script>
export default {
  name: 'PredComp',
  props: {
    msg: String
  }
} 
</script>