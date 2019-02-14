<template>
  <div>
    <h1 class="title text-center">Advantcraft</h1>

    <h3 class="text-center">A pure old-school factions server</h3>

    <!-- <p>Features among other things:</p>

    <ul class="no-list my-3">
      <li>Old school Factions</li>
      <li>PvP</li>
      <li>Griefing allowed</li>
      <li>Economy</li>
    </ul> -->

    <h2 class="mt-4">Description</h2>

    <p>Advantcraft is a pure old-school factions server. We aim to give you the classic Minecraft Factions experience. Band together with friends build a fort and forge great wars with other Factions. When supplies are low, negotiate for peace and create powerful alliances. Enjoy a solo experience? Live your life in the wilderness and try to survive on your own!</p>
    <p>There are no more plugins installed than what are necessary for a fair competitive experience. We pride ourselves in having a professional team of administrators and moderators, and have a zero-tolerance to power abuse. We never spawn in items to the game and if players fall in lava and lose everything and want their stuff back, they will have to get it themselves.</p>

    <h2 class="mt-4">Background</h2>

    <p>Advantcraft is a server that is reborn. Advantcraft was originally created back in 2011 and ran for 4 years until the two co-owners lost interest in the game, and was closed in 2015. Now 4 years later we are making a comeback, dedicated to giving our old and new players a pure Factions experience.</p>

    <p class="mt-4">The server was brought back to life in 2019-02-09. Made in Sweden.</p>

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
      tags: ["Factions", "Survival", "PVP", "Pure experience", "MC 1.13.2"]
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
