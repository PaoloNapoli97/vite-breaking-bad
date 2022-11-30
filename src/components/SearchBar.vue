<script>
import { store } from "../store.js";

export default {
  name: "SearchBar",
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <div>
    <form @change="$emit('search')">
      <div class="col-auto">
        <select
          class="form-select"
          name="category"
          v-model="store.categoryValue"
        >
          <option value="">Select Category</option>
          <option value="Breaking Bad">Breaking Bad</option>
          <option value="Better Call Saul">Better Call Saul</option>
        </select>
      </div>
    </form>
  </div>
</template>

<style lang="scss" scoped>
.form-select {
  padding: 4px;
}
</style>
