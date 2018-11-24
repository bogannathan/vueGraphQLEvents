<template>
  <div id="hello">
    <h1 class="wow fadeInDown" data-wow-delay="0.1s" 
    style="visibility: visible; animation-delay: 0.1s; animation-name: fadeInDown; color: #43b782">Event planning</h1>
    <h1>Made simple to use</h1>
    <h6>Introducing a brand new app for people who want to see what I can build</h6>
    <button class="btn btn-primary"><a style="color: white" href="mailto:bogannathan@gmail.com" target="_blank">Email me</a></button>
  </div>
</template>

<script>
export default {
  name: 'Welcome'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#hello {
  padding: 50px;
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
#hello div {
  text-align: left;
  font-size: 3vw;
  z-index: 1;
}
</style>
