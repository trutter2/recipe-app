<template>
  <div>
    <div class="wrapper">
      <div class="search">
        <form class="pure-form">
          <i class="fas fa-plus"></i><input v-model="addRecipe" placeholder="Enter New Recipe" />
        </form>
      </div>
    </div>
    <Recipes :recipes="recipes" />
  </div>
</template>

<script>
import Recipes from '../components/Recipes.vue';

export default ({
    name: "AddRecipe", 
    components: {
        Recipes,
    },
    data() {
        return{
            addRecipe: "",
        };
    },
    computed: {
        //here add what they enter into the arrary
    }
})
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