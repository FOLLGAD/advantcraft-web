<template>
  <div>
    <h1 class="title">Advantcraft</h1>
    <h3>A pure old-school factions server</h3>

    <br>

    <p>Features among other things:</p>

    <ul class="no-list my-3">
      <li>Old school Factions</li>
      <li>PvP</li>
      <li>Griefing allowed</li>
      <li>Economy</li>
    </ul>

    <p>
      This server aims to give you the classic Minecraft online server experience. Band together with friends to raid other players or try to survive on your own! Join us at advantcraft.net!
    </p>
    
    <p class="mt-4">
      The server was started on 2019-02-09. Made in Sweden 🇸🇪
    </p>

    <div class="flex mt-5 wrap">
      <div class="w-1/2 p-1">
        <img
          src="@/assets/behindtree.png"
          alt="Pic"
        >
      </div>
      <div class="w-1/2 p-1">
        <img
          src="@/assets/crossedswords.png"
          alt="Pic"
        >
      </div>
      <div class="w-1/2 p-1">
        <img
          src="@/assets/spawnarea.png"
          alt="Pic"
        >
      </div>
      <div class="w-1/2 p-1">
        <img
          src="@/assets/spawnover.png"
          alt="Pic"
        >
      </div>
    </div>

    <div class="tags">
      <el-tag
        :key="el"
        v-for="el in tags"
      >{{el}}</el-tag>
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
  },
  head() {
    return {
      title: "Advantcraft",
    }
  }
}
</script>

<style>
.tags .el-tag {
  margin-right: 5px;
}
.wrap {
  flex-wrap: wrap;
}
.no-list {
  list-style: circle;
}
</style>
