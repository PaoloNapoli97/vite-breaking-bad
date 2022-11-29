<script>
export default {
  name: "SearchBar",
};
</script>

<template>
  <div>
    <form action="">
      <div class="col-auto">
        <select class="form-select">
          <option selected>Select Category</option>
          <option value="1">One</option>
          <option value="2">Two</option>
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
