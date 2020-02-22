<template>
  <div id="sidebar-wrapper">
    <router-view></router-view>
    <ul class="nav flex-column">
      <h4 id="sidebar-header">docket</h4>
  <li class="nav-item">
    <router-link to="/" class="nav-link"><h6><img src="src/renderer/assets/icons/event-24px.svg"></h6></router-link>
  </li>
  <li id="tasks-link" class="nav-item">
    <router-link to="/tasks" class="nav-link"><h6><img src="src/renderer/assets/icons/check_circle_outline-24px.svg"></h6></router-link>
  </li>
  <li class="nav-item">
    <router-link to="/settings" class="nav-link"><h6><img src="src/renderer/assets/icons/settings-24px.svg"></h6></router-link>
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
}

#sidebar-header {
  margin-bottom: 150px;
}
</style>

