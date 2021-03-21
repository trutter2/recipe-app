<template>
  <div class="wrapper">
    <div class="products">
      <div class="product" v-for="(recipe, index) in recipes" :key="recipe.id">
        <div class="info">
          <h1>{{ recipe.name }}</h1>
          <p>Ingredients: {{ recipe.ingredients }}</p>
          <p>Time: {{ recipe.time }} mins </p>
          <button class="button" @click="deleteRecipe(index)"><i class="fas fa-trash-alt"></i></button>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: "Recipes",
  props: {
    recipes: Array,
  },
  methods: {
      deleteRecipe(index) {
        this.$root.$data.recipes.splice(index, 1);
    }
  },
};
</script>



<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.products {
  margin-top: 20px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.product {
  margin: 10px;
  margin-top: 50px;
  width: 200px;
}
.button {
    float: right;
}


.info {
  background: rgb(49, 49, 99);
  color: white;
  padding: 10px 30px;
  height: auto;
}

.info h1 {
  font-size: 16px;
}

.info h2 {
  font-size: 14px;
}

.info p {
  margin: 0px;
  font-size: 10px;
}

.price {
  display: flex;
}

button {
  height: 50px;
  background: #000;
  color: white;
  border: none;
}

.auto {
  margin-left: auto;
}
</style>