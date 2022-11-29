<script>
import axios from "axios";
import AppCard from "./AppCard.vue";

export default {
  name: "GetCharacter",
  components: {
    AppCard,
  },
  data() {
    return {
      characters: [],
    };
  },
  created() {
    axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
      this.characters = resp.data.results;
    });
  },
};
</script>

<template>
  <section>
    <div class="char-container">
      <div class="remain"><h3>Found</h3></div>
      <AppCard
        class="character-card"
        v-for="character in characters"
        :info="character"
      />
    </div>
  </section>
</template>

<style lang="scss" scoped>
.char-container {
  display: flex;
  margin-top: 20px;
  background-color: white;
  padding: 40px 20px;

  .remain {
    width: 90%;
    margin: auto;
    background-color: #212529;
    padding: 10px;
    color: white;
  }

  .character-card {
    width: calc(100% / 5);
    padding: 10px;
  }
}
</style>
