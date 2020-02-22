<template>
  <div id="tasks-content">
    <h4>Tasks</h4>
    <p id="tasks-description">Here you can see your tasks</p>
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
#tasks-content {
  background-color: rgb(247, 247, 247);
  height: 100vh;
  width: 100%;
  padding: 20px;
  padding-left: 50px;
}

#tasks-description {
  font-size: 13px;
  color: gray;
  margin-bottom: 50px;
}
</style>