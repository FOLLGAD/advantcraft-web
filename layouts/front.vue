<template>
    <div>
        <nav-bar />
		<front-header />
        <el-container class="container mx-auto">
            <el-main>
                <nuxt />
            </el-main>
            <el-aside width="250px" class="side-info">
                <server-info />
            </el-aside>
        </el-container>
        <el-footer class="mt-2">
            <div class="container mx-auto py-4 px-5 stone-bg">
                <p class="text-white">
                    Advantcraft 2019
                </p>
            </div>
        </el-footer>
    </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue'
import FrontHeader from '@/components/FrontHeader.vue'
import ServerInfo from '@/components/ServerInfo.vue'
export default {
	components: {
		NavBar,
        FrontHeader,
        ServerInfo,
	},
}
</script>


<style>
h1, h2, h3 {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
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
.side-info {
    background-color: #fafafa;
    width: 200px;
    margin-left: 15px;
    padding: 15px;
}
.stone-bg {
    background-image: url("../assets/stone-tile.png");
    background-size: auto;
    background-repeat: repeat;
}
</style>
