<template>
  <div>
    <div class="wrapper">
      <div class="search">
        <form v-on:submit.prevent="onSubmit" class="pure-form">
          <i class="fas fa-plus"></i>
          <input v-model="name" placeholder="Enter New Recipe" />
          <div class="ingredients">
            <input v-model="ingredients" placeholder="Enter Ingredients seperated by comma" />
          </div>
          <div class="time">
            <input v-model="time" placeholder="Enter Time"/>
          </div>
          <button @click="addRecipe" class="pure-button sideby">
            Add Recipe
          </button>
        </form>
      </div>
    </div>
    <Recipes :recipes="recipes" />
  </div>
</template>

<script>
import Recipes from "../components/Recipes.vue";

export default {
  name: "AddRecipe",
  components: {
    Recipes,
  },
  data() {
    return {
      name: "",
      time: null,
      ingredients: "",
    };
  },
  computed: {
    recipes() {
      return this.$root.$data.add;
    },
  },
  methods: {
    addRecipe() {
      this.$root.$data.recipes.push({
        id: (this.$root.$data.length + 1),
        name: this.name,
        ingredients: this.ingredients,
        time: parseInt(this.time),
      });
      alert("recipe added!")
      this.name = "";
      this.ingredients = "";
      this.time = null;
    },
  },
};
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
  width: 75%;
  padding: 3px;
}
.ingredients {
  border: 1px solid #ccc;
  border-radius: 4px;
  width: 50%;
  margin: 3px;
  float: left;
}
.time {
  border: 1px solid #ccc;
  border-radius: 4px;
  width: 25%;
  margin: 3px;
  float: left;
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