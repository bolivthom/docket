<template>
  <div id="content-wrapper">
    <h1>HI THERE. I'M A TIMETABLE</h1>
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
#content-wrapper {
  margin: 20px;
}
</style>