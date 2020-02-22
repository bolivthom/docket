<template>
  <div id="">
    <main>
      <div class="left-side">
        <tasksSidebar></tasksSidebar>
        <tasks></tasks>
      </div>
      <div class="right-side">
      </div>
    </main>
  </div>
</template>

<script>
  import tasksSidebar from './sidebar/tasksSidebar'
  import tasks from './sidebarContent/tasks'

  export default {
    name: 'tasks-page',
    components: { tasksSidebar, tasks },
    methods: {
      open (link) {
        this.$electron.shell.openExternal(link)
      }
    }
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body { font-family: 'Source Sans Pro', sans-serif; }

  #wrapper {
    background:
      radial-gradient(
        ellipse at top left,
        rgba(255, 255, 255, 1) 40%,
        rgba(229, 229, 229, .9) 100%
      );
    height: 100vh;
    width: 100vw;
  }

  

  main {
    display: flex;
    justify-content: space-between;
  }

  main > div { flex-basis: 50%; }

  .left-side {
    display: flex;
    flex-direction: row;
  }

</style>
