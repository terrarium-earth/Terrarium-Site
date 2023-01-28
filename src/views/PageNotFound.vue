<template>
  <div class="container">
    <h1 class="title">404</h1>
    <h2 class="subtitle">Page not found</h2>
    <p class="text">
      The page you are looking for does not exist. Please check the URL and try
      again.
    </p>
  </div>
</template>

<script>
export default {
  name: "PageNotFound",
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  text-align: center;
}
</style>
