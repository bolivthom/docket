<template>
  <div id="settings-content">
    <router-link id="close-icon" to="/" class="nav-link"><svg xmlns="http://www.w3.org/2000/svg" height="24" viewBox="0 0 24 24" width="24"><path d="M0 0h24v24H0V0z" fill="none"/><path d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12 19 6.41z"/></svg></router-link>
    <h4>New Lesson</h4>
    <p id="new-schedule-description">Here you can create a new lesson and add it to your timetable</p>
    
    <form>
  <div id="left" class="form-group">
    <label>Lesson Name</label>
    <input type="text" class="form-control" id="">
  </div>
  <div class="form-group">
    <label>Day</label>
    <select type="text" class="form-control" id="">
        <option>Monday</option>
        <option>Tuesday</option>
        <option>Wednesday</option>
    </select>
  </div>
  
  <div id="left" class="form-group">
    <label>Start Time</label>
    <input type="time" class="form-control" id="">
  </div>
  <div class="form-group">
    <label>End Time</label>
    <input type="time" class="form-control" id="">
  </div>
  
  <div id="left" class="form-group">
    <label>Location</label>
    <input type="text" class="form-control" id="">
  </div>
  <div class="form-group">
    <label>Teacher</label>
    <input type="text" class="form-control" id="">
  </div>
  
    <button type="button"  id="add-schedule-button">SUBMIT</button>
</form>
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
#close-icon {
    fill: darkgray;
    float: right;
}

#close-icon:hover {
    fill: #AD1457;
}

#new-schedule-description {
    font-size: 13px;
    color: gray;
    margin-bottom: 50px;
}

label {
    font-size: 13px;
    color: gray;
}

input, select {
    outline: none !important;
    border: none !important;
}

input:focus, select:focus {
    outline: none !important;
    border: none !important;
    -webkit-box-shadow: none !important;
    box-shadow: none !important;
}

#add-schedule-button {
  height: 40px;
  width: 100px;
  background-color: #AD1457;
  border: none;
  border-radius: 4px;
  color: white;
  font-size: 12px;
  font-weight: 500;
}

form {
  width: 500px;
  margin-bottom: 50px;
}
</style>