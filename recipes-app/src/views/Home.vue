<template>
  <div>
    <div class="wrapper">
      <h1>Welcome!</h1>
    </div>
    <p class="wrapper">
      This site allows you to store recipes that you like! just click on the add
      recipes in the top right to get started! or browse recipes under the recipes tab!
    </p>
  </div>
</template>

<script>
</script>

<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.search {
  border: 1px solid #ccc;
  border-radius: 4px;
  width: 50%;
}

form {
  display: table;
  width: 100%;
}

i {
  display: table-cell;
  padding-left: 10px;
  width: 1px;
}

input {
  display: table-cell;
  font-size: 20px;
  border: none !important;
  box-shadow: none !important;
  width: 100%;
  height: 40px;
}
</style>