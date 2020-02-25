<template>
  <div id="settings-content">
    <h4>Settings</h4>
    <p id="settings-description">You can change your preferences here. They will be automatically saved.</p>
    <div>

      <p id="theme-header">Theme</p>
      <div id="theme-settings">
        <div id="dark-theme">
          <div class="card border-0">
            <div class="card-body">
            </div>
          </div>
          <p class="theme-title">Dark</p>
        </div>

        <div id="light-theme"> 
          <div class="card border-0">
            <div class="card-body">
            </div>
          </div>
          <p class="theme-title">Light</p>
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
  padding-left: 50px;
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
  margin-right: 100px;
}

.card {
  height: 150px;
  width: 150px;
}

.theme-title {
  font-size: 13px;
  color: gray;
  text-align: center;
  padding: 10px;
}

</style>