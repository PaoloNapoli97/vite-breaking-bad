<script>
export default {
  name: "AppHeader",
};
</script>

<template>
  <header>
    <div class="logo">
      <img src="../assets/logo.png" alt="" />
      <h1>Breaking Bad Api</h1>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  color: white;
  padding: 10px;
  margin-bottom: 40px;

  .logo {
    display: flex;
    height: 40px;
    align-items: center;

    img {
      height: 100%;
      padding-right: 10px;
    }
  }
}
</style>
