<template>
  <div id="app">
    <div id="menu">
      <div id="brand">
        <router-link to="/">
          <img src="../images/myRecipes.jpg" />
        </router-link>
      </div>
      <div id="side">
        <router-link to="/recipes">
          <div class="menu-item browse">
            <img src="../images/book.jpeg" />
            <p>Recipes</p>
          </div>
        </router-link>
        <router-link to="/addrecipe">
          <div class="menu-item">
            <img src="../images/plus.png" />
            <p>Add</p>
          </div>
        </router-link>
      </div>
    </div>
    <router-view />
    <br><br><br>
    <div class="footer">
        <a href="https://github.com/trutter2/recipe-app.git"> <i class="fab fa-github" ></i></a>
    </div>
  </div>
</template>



<style>
* {
  box-sizing: border-box;
}

body {
  margin: 50px 100px;
}

#menu {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-column-gap: 5px;
  grid-template-areas: "none brand side";
  margin-bottom: 50px;
}

#menu a {
  color: #b84901;
}

#brand {
  grid-area: brand;
  display: flex;
  justify-content: center;
}

#brand img {
  height: 200px;
}

#side {
  grid-area: side;
  display: flex;
  justify-content: flex-end;
}

#side img {
  width: 50px;
}

.menu-item {
  display: flex;
  flex-direction: column;
}
.menu-item:hover {
  opacity: 0.2;
}
.menu-item p {
  margin: 0px;
}

.browse {
  margin-right: 50px;
}
.footer {
    position: fixed;
    left: 0;
    bottom: 0;
    width: 100%;
    background-color: rgb(49, 49, 99);
    color: white;
    text-align: center;
    justify-content: left;
}

.fab:hover {
    opacity: 0.2;
    color: white;
}
</style>

