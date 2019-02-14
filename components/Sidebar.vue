<template>
  <div>
    <div class="center info-box">
      <div>
        Server status <el-tag
          type="success"
          v-if="players !== null"
        >{{players}}/{{max}} playing</el-tag>
      </div>
      <div class="ip-address bg-grey-lighter rounded py-2 px-3">
        <el-tooltip
          effect="dark"
          class="item"
          placement="left"
          content="Copy"
          v-clipboard:copy="ip"
        >
          <span>IP: {{ip}}</span>
        </el-tooltip>
      </div>
    </div>
    <div class="info-box">
      <h2 class="text-center">Rules</h2>
      <ol class="rules">
        <li>No unfair modifications of the game client allowed.</li>
        <li>No spamming.</li>
        <li>No exploiting bugs or glitches.</li>
        <li>Hold cursing to a minimum.</li>
        <li>No advertising on the server.</li>
      </ol>
    </div>
    <div class="info-box center text-sm">
      Oh yeah yeah
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
.info-box {
  background-color: #fafafa;
  margin-bottom: 10px;
  padding: 15px;
}
.rules li {
  margin-top: 5px;
}
</style>
