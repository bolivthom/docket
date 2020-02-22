<template>
  <div id="settings-content">
    <h4>Settings</h4>
    <p id="settings-description">You can change your preferences here. They will be automatically saved.</p>
    <div>
      <p id="theme-header">Theme</p>
      <div id="theme-settings">
        <div id="dark-theme">
          <p>Dark</p>
        </div>
        <div id="light-theme">
          <p>Light</p>
        </div>
      </div>
    </div>
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
#settings-content {
  background-color: rgb(247, 247, 247);
  height: 100vh;
  width: 100%;
  padding: 20px;
}

#settings-description {
  font-size: 13px;
  color: gray;
  margin-bottom: 50px;
}

#theme-header {
  font-size: 20px;
}

#theme-settings {
  display: flex;
  flex-direction: row;
}

#dark-theme {
  margin-right: 200px;
}
</style>