<template>
  <div class="root">
    <div class="header">
      <router-link to="/" class="logo no-animation">
        <img
          class="logo"
          src="@/assets/terrariumlogo.png"
          alt="terrarium logo"
        />
      </router-link>
      <nav>
        <router-link to="/">Home</router-link>
        <router-link to="/news">News</router-link>
        <router-link to="/projects">Projects</router-link>
        <router-link to="/content-creators">Content Creators</router-link>
        <router-link to="/contact">Contact</router-link>
      </nav>
    </div>
    <div class="slot">
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
  padding: 32px 0;
  vertical-align: center;
  width: 100%;
}

nav > a {
  display: inline-block;
  padding: 8px 16px;
  font-size: var(--text-nav-font-size);
  height: 100%;
  text-decoration: none;
  vertical-align: center;
}

.logo {
  height: 100%;
  border-radius: 100%;
  aspect-ratio: 1/1;
}

/* make fixed in place */
.root {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin: 0 10%;
  vertical-align: center;
  height: 100%;
}

nav {
  vertical-align: center;
}

.slot {
  height: 100%;
  width: 100%;
}
</style>
