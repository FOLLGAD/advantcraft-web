<template>
    <div class="center">
        <div>
            Server status <el-tag type="success">3 online</el-tag>
        </div>
        <div class="ip-address">
            <el-tooltip effect="dark" class="item" placement="left" content="Copy" v-clipboard:copy="ip">
                <span>IP: {{ip}}</span>
            </el-tooltip>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            ip: "192.168.1.20",
        }
    }
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
