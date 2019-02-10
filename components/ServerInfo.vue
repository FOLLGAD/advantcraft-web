<template>
  <div class="center">
    <div>
      Server status <el-tag type="success" v-if="players !== null">{{players}}/{{max}} playing</el-tag>
    </div>
    <div class="ip-address bg-grey-lighter rounded py-2 px-3">
      <el-tooltip
        effect="dark"
        class="item"
        placement="left"
        content="Copy"
        v-clipboard:copy="ip"
      >
        <span class="">IP: {{ip}}</span>
      </el-tooltip>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      ip: "advantcraft.net",
      players: null,
      max: null,
    }
  },
  mounted() {
    var url = "https://api.minetools.eu/ping/" + this.ip;
    fetch(url)
      .then(val => val.json())
      .then(json => {
        this.players = json.players.online;
        this.max = json.players.max;
      })
  },
}
</script>

<style scoped>
.center {
  display: flex;
  align-content: center;
  align-items: center;
  flex-direction: column;
}
.ip-address {
  cursor: pointer;
  font-size: 1.7rem;
  margin-top: 10px;
}
</style>
