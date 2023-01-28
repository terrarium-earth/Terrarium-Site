<template>
  <HeaderBanner></HeaderBanner>
  <router-view />
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
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

body {
  margin: 0;
}
</style>
<script>
import HeaderBanner from "@/components/HeaderBanner";
export default {
  components: { HeaderBanner },
};
</script>
