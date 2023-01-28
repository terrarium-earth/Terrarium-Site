<template>
  <HeaderBanner>
    <router-view />
  </HeaderBanner>
</template>

<style>
/*noinspection CssUnknownTarget*/
@import url("https://fonts.googleapis.com/css2?family=Fredoka+One&family=Pacifico&display=swap");
/*noinspection CssUnknownTarget*/
@import url("https://fonts.googleapis.com/css2?family=Poppins&display=swap");
#app {
  font-family: Poppins, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
  width: 100%;
}

:root {
  --primary-font: "Fredoka One", sans-serif;
  --secondary-font: "Poppins", sans-serif;
  --title-font-size: 128px;
  --title-secondary-font-size: 64px;
  --subtitle-font-size: 32px;
  --text-font-size: 24px;
  --text-nav-font-size: 16px;
}

nav a {
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #448d67;
}

body {
  margin: 0;
  background-color: #bae5c5;
  height: 100%;
}

html {
  height: 100%;
}

a {
  display: inline-block;
  text-decoration: none;
}

a:not(.no-animation)::after {
  content: "";
  display: block;
  margin: auto;
  width: 0;
  height: 2px;
  background: #2c3e50;
  transition: width 0.3s ease;
}

.left-ease:not(.no-animation)::after {
  margin: unset;
}

a:not(.no-animation):hover::after {
  width: 100%;
}

a.router-link-exact-active::after {
  width: 100%;
  background: #448d67;
}

a:visited {
  text-decoration: none;
  color: #2c3e50;
}
</style>
<script>
import HeaderBanner from "@/components/HeaderBanner";
export default {
  components: { HeaderBanner },
};
</script>
