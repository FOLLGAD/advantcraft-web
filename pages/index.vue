<template>
  <div>
    <h1 class="title">Advantcraft</h1>
    <h3>A pure old-school factions server</h3>

    <p>Join our minecraft server</p>

    <div class="flex mt-5">
      <div class="w-1/2 mr-1">
        <img src="https://proxy.duckduckgo.com/iu/?u=https%3A%2F%2Fminecraft.fr%2Fforum%2Fattachments%2F2014-07-11_17-20-17-png.37636%2F&f=1" alt="Pic">
      </div>
      <div class="w-1/2">
        <img src="https://proxy.duckduckgo.com/iu/?u=http%3A%2F%2Fimage.noelshack.com%2Ffichiers%2F2016%2F48%2F1480865738-spawn.png&f=1" alt="Pic">
      </div>
    </div>

    <div class="tags">
      <el-tag :key="el" v-for="el in tags">{{el}}</el-tag>
    </div>
  </div>
</template>

<script>
export default {
  layout: "front",
  data() {
    return {
      tags: ["Factions", "Survival", "PVP", "Pure experience"]
    }
  }
}
</script>

<style>
.tags .el-tag {
  margin-right: 5px;
}
</style>
