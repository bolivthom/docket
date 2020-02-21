<template>
  <div>
    <ul class="nav flex-column">
  <li class="nav-item">
    <a class="nav-link active" href="/">Timetable</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="/tasks">Tasks</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="/settings">Settings</a>
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

