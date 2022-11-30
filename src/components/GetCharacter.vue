<script>
import { store } from "../store";

import AppCard from "./AppCard.vue";

export default {
  name: "GetCharacter",
  components: {
    AppCard,
  },
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <section>
    <div class="char-container">
      <div class="remain">
        <h3>Found {{ store.characters.length }} characters</h3>
      </div>
      <div class="cards-container" v-if="store.characters.length > 0">
        <AppCard
          class="character-card"
          v-for="character in store.characters"
          :info="character"
        />
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.char-container {
  display: flex;
  margin-top: 20px;
  background-color: white;
  padding: 40px 20px;
  flex-direction: column;

  .remain {
    width: 90%;
    margin: auto;
    background-color: #212529;
    padding: 10px;
    color: white;
  }

  .cards-container {
    margin-top: 20px;
    display: flex;
    flex-wrap: wrap;
    .character-card {
      margin: 15px;
      width: calc((100% / 5) - 30px);
    }
  }
}
</style>
