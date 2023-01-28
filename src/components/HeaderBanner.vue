<template>
  <div class="root">
    <div class="header">
      <img class="logo" src="@/assets/terrariumlogo.png" />
      <ul>
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/about">What we do</router-link></li>
        <li><router-link to="/about">Projects</router-link></li>
        <li><router-link to="/about">Content Creators</router-link></li>
        <li><router-link to="/about">Contact</router-link></li>
      </ul>
    </div>
    <div>
      <slot />
    </div>
  </div>
</template>

<script>
export default {
  name: "HeaderBanner",
};
</script>

<style scoped>
/*noinspection CssUnknownTarget*/
@import url("https://fonts.googleapis.com/css2?family=Pacifico&display=swap");
/*noinspection CssUnknownTarget*/
@import url("https://fonts.googleapis.com/css2?family=Poppins&display=swap");

.header {
  height: 64px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin: 24px;
  vertical-align: center;
}

li {
  display: inline-block;
  padding: 8px 16px;
  font-size: 16px;
}

.logo {
  height: 96px;
  width: 96px;
  border-radius: 100%;
}

.root {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin: 0;
  vertical-align: center;
  background-color: #bae5c5;
}

a {
  text-decoration: none;
  font-size: 16px;
}
</style>
