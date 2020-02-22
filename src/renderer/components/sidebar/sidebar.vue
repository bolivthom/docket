<template>
  <div id="sidebar-wrapper">
    <router-view></router-view>
    <ul class="nav flex-column">
  <li class="nav-item">
    <router-link to="/" class="nav-link">Home</router-link>
  </li>
  <li class="nav-item">
    <router-link to="/tasks" class="nav-link">Tasks</router-link>
  </li>
  <li class="nav-item">
    <router-link to="/settings" class="nav-link">Settings</router-link>
  </li>
</ul>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        electron: process.versions.electron,
        name: this.$route.name,
        node: process.versions.node,
        path: this.$route.path,
        platform: require('os').platform(),
        vue: require('vue/package.json').version
      }
    }
  }
</script>

<style>
#sidebar-wrapper {
  padding: 20px;
  width: 300px;
}


#tasks-link, #settings-link {
  color: darkgray;
}
</style>

