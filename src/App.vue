<template>
  <div id="app">
    <main>
      <div class="search__box">
        <input type="text" class="search__bar" placeholder="Search..." />
      </div>
      <div class="weather__wrap">
        <div class="location__box">
          <div class="location">Perris, CA, USA</div>
          <div class="location__date">Friday, May 29, 2020</div>
        </div>
        <div class="weather__box">
          <div class="weather__temp">105°F</div>
          <div class="weather">Hot</div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      api_key: "0e82bb16227c1a3b88661dd32729d7b1"
    };
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600;700&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "Open Sans", sans-serif;
}

#app {
  background-image: url(./assets/cold-bg.jpg);
  background-size: cover;
  background-position: bottom;
  transition: 0.4s;
}
main {
  min-height: 100vh;
  padding: 2.5rem;
  background-image: linear-gradient(
    to bottom,
    rgba(0, 0, 0, 0.25),
    rgba(0, 0, 0, 0.75)
  );
}

.search__box {
  width: 100%;
  margin-bottom: 3rem;
}

.search__box .search__bar {
  display: block;
  width: 100%;
  padding: 15px;
  color: #313131;
  font-size: 2rem;
  appearance: none;
  border: none;
  outline: none;
  background: none;
  box-shadow: 0px 0px 8px rgba(0, 0, 0, 0.25);
  background-color: rgba(255, 255, 255, 0.5);
  border-radius: 0px 16px 0px 16px;
  transition: 0.4s;
}
.search__box .search__bar:focus {
  background-color: rgba(255, 255, 255, 0.75);
  box-shadow: 0px 0px 16px rgba(0, 0, 0, 0.25);
  border-radius: 16px 0px 16px 0px;
}

.location__box .location {
  color: white;
  font-size: 32px;
  font-weight: 500;
  text-align: center;
  text-shadow: 1px 3px rgba(0, 0, 0, 0.25);
}

.location__box .location__date {
  color: #fff;
  font-size: 20px;
  font-weight: 300;
  font-style: italic;
  text-align: center;
}

.weather__box {
  text-align: center;
}
.weather__box .weather__temp {
  display: inline-block;
  padding: 10px 25px;
  color: #fff;
  font-size: 102px;
  font-weight: 900;
  text-shadow: 3px 6px rgba(0, 0, 0, 0.25);
  background-color: rgba(255, 255, 255, 0.25);
  border-radius: 16px;
  margin: 30px 0px;
}
</style>
