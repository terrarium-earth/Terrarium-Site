<template>
  <div class="stat">
    <p class="stat-title">
      {{ title }}
    </p>
    <p class="stat-subtitle">
      {{ subtitle }}
    </p>
  </div>
</template>

<script>
export default {
  name: "StatComponent",
  props: {
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.stat-title {
  font-size: 48px;
  font-family: Fredoka One;
  margin: 0;
  padding: 0;
  font-weight: bold;
}

.stat-subtitle {
  font-size: 24px;
  font-family: Poppins;
  text-align: center;
  margin: auto;
  color: #4a7263;
}

.stat {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin: 24px 0 24px 0;
  vertical-align: center;
  text-align: center;
}
</style>
