<template>
  <header>
    <div class="flex">
      <h1>logo</h1>
      <Burger />
    </div>
    <Sidebar>
      <ul class="sidebar-panel-nav">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </Sidebar>
  </header>
</template>

<script>
import Burger from "./Burger.vue";
import Sidebar from "./Sidebar.vue";

export default {
  name: "header",
  components: { Burger, Sidebar },
};
</script>

<style lang="scss" scoped>
@import "@/scss/_variables.scss";
header{
     padding: 0.5rem 0.8rem;
}
.flex {
  display: flex;
  justify-content: space-between;
}
 ul.sidebar-panel-nav {
   list-style-type: none;
 }

 ul.sidebar-panel-nav > li > a {
   color: $primary-color;
   text-decoration: none;
   font-size: 1.5rem;
   display: block;
   padding-bottom: 0.5em;
 }
</style>