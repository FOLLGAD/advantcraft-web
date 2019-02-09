<template>
    <div>
        <el-container class="hidden-xs-only">
            <div class="header container mx-auto">
                <h2 class="brand">Advantcraft</h2>
                <ul>
                    <li><nuxt-link exact to="/">Home</nuxt-link></li>
                    <li><nuxt-link to="/donate">Donations</nuxt-link></li>
                </ul>
                <div class="right">
                    <ul>
                        <li><a href="https://discord.gg/r5dVpnQ" target="_blank">Join our Discord</a></li>
                    </ul>
                </div>
            </div>
        </el-container>
        <div class="hidden-sm-and-up w-full flex bg-white relative z-5">
            <div class="top-menu inline-block" @click="toggleMobileMenu">
                <!-- Menu button svg -->
                <svg class="menu-btn" height="32px" id="Layer_1" version="1.1" viewBox="0 0 32 32" width="32px" xml:space="preserve" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><path d="M4,10h24c1.104,0,2-0.896,2-2s-0.896-2-2-2H4C2.896,6,2,6.896,2,8S2.896,10,4,10z M28,14H4c-1.104,0-2,0.896-2,2  s0.896,2,2,2h24c1.104,0,2-0.896,2-2S29.104,14,28,14z M28,22H4c-1.104,0-2,0.896-2,2s0.896,2,2,2h24c1.104,0,2-0.896,2-2  S29.104,22,28,22z"/></svg>
            </div>
        </div>
        <div class="w-full hidden-sm-and-up relative">
            <el-menu :class="{ open: mobileMenuOpen }">
                <el-menu-item index="1"><nuxt-link exact to="/">Home</nuxt-link></el-menu-item>
                <el-menu-item index="2"><nuxt-link to="/donate">Donations</nuxt-link></el-menu-item>
                <el-menu-item index="3"><a href="https://discord.gg/r5dVpnQ" target="_blank">Join our Discord</a></el-menu-item>
            </el-menu>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            mobileMenuOpen: false,
        }
    },
    methods: {
        toggleMobileMenu() {
            this.mobileMenuOpen = !this.mobileMenuOpen;      
        }
    }
}
</script>


<style scoped>
.big {
    font-size: 1.2em;
}
.header {
    width: 100%;
    background-color: #eeeeee10;
    /* padding: 20px 15px; */
}
.header li * {
    padding: 20px 15px;
    display: block;
    color: black;
    text-decoration: none;
    transition: all 150ms;
    border-bottom: rgba(90, 175, 255, 0) 2px solid;
}
.header li *.nuxt-link-active {
    background-color: #e6e6e61c;
    border-bottom: rgb(90, 175, 255) 2px solid;
}
.header li:hover * {
    background-color: #e6e6e63a !important;
}
.header {
    display: flex;
    flex-direction: row;
}
.header ul {
    display: flex;
    flex-direction: row;
    list-style: none;
    padding: 0;
}
.brand {
    margin: auto 30px;
}
.right {
    margin-left: auto;
}
.el-menu {
    width: 100%;
    margin-top: -100%;
    transition: 500ms margin linear;
    position: absolute;
    float: right;
    top: 0;
}
.el-menu.open {
    margin-top: 0;
}
.top-menu {
    z-index: 100;
    padding: 10px;
    display: inline-block;
    margin-left: auto;
    cursor: pointer;
}
.z-5 {
    z-index: 5;
}
</style>
