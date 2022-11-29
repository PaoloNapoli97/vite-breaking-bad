<script>
import SearchBar from "./SearchBar.vue";
import GetCharacter from "./GetCharacter.vue";

export default {
  name: "AppMain",
  components: {
    SearchBar,
    GetCharacter,
  },
};
</script>

<template>
  <main>
    <div class="container">
      <SearchBar />
      <GetCharacter />
    </div>
  </main>
</template>

<style lang="scss" scoped></style>
