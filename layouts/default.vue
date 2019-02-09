<template>
	<div>
		<nav-bar />
		<front-header />
		<el-container class="container mx-auto">
			<el-main>
				<nuxt />
			</el-main>
		</el-container>
	</div>
</template>

<script>
import "../assets/tailwind.min.css"
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
html {
	/* background-color: rgb(253, 251, 245); */
}
body {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI",
    Roboto, "Helvetica Neue", Arial, sans-serif;
  word-spacing: 1px;
	overflow-y: scroll;
}

.center-container {
  max-width: 1100px;
  width: 100%;
  margin-left: auto;
  margin-right: auto;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
</style>
