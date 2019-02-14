<template>
  <div>
    <nav-bar />
    <front-header />
    <el-container class="container mx-auto mt-2 phone-flex">
      <el-main>
        <nuxt />
      </el-main>
      <aside class="side-bar">
        <sidebar />
      </aside>
    </el-container>
    <el-container>
      <el-footer class="mt-2">
        <div class="container mx-auto py-4 px-5 stone-bg">
          <p class="text-white">
            Advantcraft 2019
          </p>
        </div>
      </el-footer>
    </el-container>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue'
import FrontHeader from '@/components/FrontHeader.vue'
import Sidebar from '@/components/Sidebar.vue'
export default {
  components: {
    NavBar,
    FrontHeader,
    Sidebar,
  },
}
</script>

<style>
@media (max-width: 767px) {
  .phone-flex {
    display: flex;
    flex-direction: column-reverse;
  }
  aside.side-bar {
    margin-left: 0px;
    width: 100%;
  }
}

.side-bar {
  box-sizing: border-box;
  flex-shrink: 0;
  width: 300px;
  margin-left: 15px;
}

h1,
h2,
h3 {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-weight: 300;
  color: #35495e;
  letter-spacing: 1px;
}

.title {
  font-size: 64px;
}

html {
  background-color: #f3f3f3;
}
.el-main {
  background-color: #ffffff;
}
.stone-bg {
  background-image: url("../assets/stone-tile.png");
  background-size: auto;
  background-repeat: repeat;
}
</style>
