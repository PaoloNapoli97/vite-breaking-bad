<script>
export default {
  name: "AppCard",
  props: {
    info: Object,
  },
};
</script>

<template>
  <div class="card">
    <img :src="info.img" :alt="info.name" />
    <h3>{{ info.name }}</h3>
    <div class="info">
      <div class="serie">{{ info.category }}</div>
      <div class="status">{{ info.status }}</div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  text-align: center;
  padding: 10px;
  color: white;
  background-color: #2e3a46;

  img {
    width: 100%;
    height: 200px;
    object-fit: contain;
  }

  h3 {
    padding: 10px 0;
  }

  .info {
    color: gray;
    padding-bottom: 30px;
  }
}
</style>
