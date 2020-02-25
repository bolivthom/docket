<template>
  <div id="tasks-content">
    <button type="button" v-on:click="addTask()" class="tasks-add-button">
    <svg id="tasks-plus-icon" xmlns="http://www.w3.org/2000/svg" height="24" viewBox="0 0 24 24" width="24"><path d="M0 0h24v24H0V0z" fill="none"/><path d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"/></svg>
    </button>
    <h4>Tasks</h4>
    <p id="tasks-description">Here you can create your tasks</p>
    <div v-for="(task, index) in tasks" :key="index">
      <task v-bind="Task"></task>
    </div>
  </div>
</template>

<script>
let Task = {
  template: `<div id="task">
              <svg id="task-point-outline" xmlns="http://www.w3.org/2000/svg" height="24" viewBox="0 0 24 24" width="24"><path d="M0 0h24v24H0V0z" fill="none"/><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 18c-4.42 0-8-3.58-8-8s3.58-8 8-8 8 3.58 8 8-3.58 8-8 8z"/></svg>
              <input v-on:keyup.return="addTask()" type="text" id="task-input">
              </div>`
}

export default {
  el: '#components-demo',
  data () {
    return {
      electron: process.versions.electron,
      name: this.$route.name,
      node: process.versions.node,
      path: this.$route.path,
      platform: require('os').platform(),
      vue: require('vue/package.json').version,
      tasks: []
    }
  },
  components: {
    Task
  },
  methods: {
    addTask () {
      this.tasks.push(Task)
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

.tasks-add-button {
  float: right;
  top: 0;
  height: 40px;
  width: 100px;
  background-color: #AD1457;
  border: none;
  border-radius: 4px;
}

#tasks-plus-icon {
  fill: white;
  height: 2opx;
  width: 20px;
}

button:focus {
    outline: none !important;
    border: none !important;
    -webkit-box-shadow: none !important;
    box-shadow: none !important;
}

#task{
  display: flex;
  flex-direction: row;
  margin-bottom: 15px;
  color: gray;
}

#task-point-outline{
  padding-right: 5px;
  fill: #AD1457;
}

#task-input {
  background: rgb(247, 247, 247);
  width: 100%;
}
</style>