<template>
  <div id="">
    <main>
      <div class="left-side">
        <div id="x">
        <timetableSidebar></timetableSidebar>
        </div>
        <tasks></tasks>
      </div>
      <div class="right-side">
      </div>
    </main>
  </div>
</template>

<script>
  import timetableSidebar from './sidebar/timetableSidebar'
  import tasks from './sidebarContent/newSchedule'

  export default {
    name: 'new-schedule-page',
    components: { timetableSidebar, tasks },
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
    height: 100v;
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
