<template>
  <div id="timetable-content">
    <router-link to="/new-schedule">
    <button type="button" class="timetable-add-button">
      <svg id="timetable-plus-icon" xmlns="http://www.w3.org/2000/svg" height="24" viewBox="0 0 24 24" width="24"><path d="M0 0h24v24H0V0z" fill="none"/><path d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"/></svg>
    </button>
    </router-link>
    <h4>Timetable</h4>
    <p id="timetable-description">Here you can view your weekly schedule</p>
    <div id="timetable-days">
      <div class="row">
        <div class="col-sm">
          MONDAY
        </div>
        <div class="col-sm">
          TUESDAY
        </div>
        <div class="col-sm">
          WEDNESDAY
        </div>
        <div class="col-sm">
          THURSDAY
        </div>
        <div class="col-sm">
          FRIDAY
        </div>
        <div class="col-sm">
          SATURDAY
        </div>
        <div class="col-sm">
          SUNDAY
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
#timetable-content {
  background-color: rgb(247, 247, 247);
  height: 100vh;
  width: 100%;
  padding: 20px;
  padding-left: 50px;
}

#timetable-description {
  font-size: 13px;
  color: gray;
  margin-bottom: 50px;
}


.timetable-add-button {
  float: right;
  top: 0;
  border-radius: 50%;
  height: 40px;
  width: 100px;
  background-color: #AD1457;
  border: none;
  border-radius: 4px;
}

#timetable-plus-icon {
  fill: white;
  height: 2opx;
  width: 20px;
}

#timetable-days {
  font-size: 13px;
  color: gray;
}
</style>