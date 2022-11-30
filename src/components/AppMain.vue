<script>
import axios from "axios";
import { store } from "../store.js";

import SearchBar from "./SearchBar.vue";
import GetCharacter from "./GetCharacter.vue";

export default {
  name: "AppMain",
  components: {
    SearchBar,
    GetCharacter,
  },
  data() {
    return {
      store,
    };
  },
  methods: {
    getCharacters() {
      axios
        .get("https://www.breakingbadapi.com/api/characters", {
          params: {
            category: this.store.categoryValue,
          },
        })
        .then((resp) => {
          this.store.characters = resp.data;
        })
        .catch((err) => {
          this.store.characters = [];
        });
    },

    created() {
      this.getCharacters();
    },
  },
};
</script>

<template>
  <main>
    <div class="container">
      <SearchBar @search="getCharacters" />
      <GetCharacter />
    </div>
  </main>
</template>

<style lang="scss" scoped></style>
