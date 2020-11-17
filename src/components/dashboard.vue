<template>
  <main>
    <header>
      <!-- <h1>USER DASHBOARD</h1> -->
      <TopNav />
    </header>
    <div>
      <div class="sidebar">
        <SideBar />
      </div>
      <div class="main-page relative">
        <router-view></router-view>
        
      </div>
    </div>
  </main>
</template>

<script>
import SideBar from "./side-bar/side-bar.vue";
import TopNav from "./top-nav/top-nav.vue";
export default {
  name: "Dashboard",
  components: { SideBar,TopNav },
};
</script>

<style scoped>
 /* main > header {
  width: 100%;
  height: 7%;
} */

/* main {
  height: 100vh;
}  */

/* main > div {
  height: 93%;
  display: flex;
} */

</style>
