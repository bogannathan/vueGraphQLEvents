<template>
  <div id="app">
    <div id="nav">
      <div class="container">
      <span id="title">nathan's events</span>
      <div id="siteLinks">
        <router-link to="/">Home</router-link> |
        <router-link to="/events">Events</router-link> |
        <router-link to="/addevent">Add Event</router-link>
      </div>
      </div>
    </div>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  border-bottom: 5px solid #fafafa;
}

#nav a,
span {
  font-weight: bold;
  color: #2c3e50;
}

.container {
  padding: 15px;
  display: flex;
  align-content: center;
  justify-content: space-between;
}

#nav a.router-link-exact-active {
  color: #ffb95d;
}

#title {
  color: #43b782;
}

#siteLinks {
  display: flex;
  -ms-flex-align: center;
  align-items: center;
  -ms-flex-line-pack: center;
  align-content: center;
  -ms-flex-pack: justify;
  justify-content: space-between;
  width: auto;
  max-width: 450px;
}

#siteLinks a,
#title {
  padding: 0 20px;
  font-size: 22px;
}
</style>
