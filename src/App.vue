<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  },
};
</script>

<template>
  <main>
    <AppHeader />
    <AppMain />
    <AppFooter />
  </main>
</template>

<style lang="scss">
@import "./styles/global.scss";
</style>
