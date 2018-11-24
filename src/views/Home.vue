<template>
  <div class="home">
    <div class="banner">
      <div style="flex: 1; display: flex; flex-direction: column">
        <Welcome />
      </div>
      <div id="calendar">
      <div id="calendarImg"><img src="../assets/calendar.jpg" /></div>
      </div>
    </div>
    <div class="content">
      <WhyUse />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Welcome from '@/components/Welcome.vue'
import WhyUse from '@/components/WhyUse/WhyUse.vue'

export default {
  name: 'home',
  components: {
    Welcome,
    WhyUse
  }
}
</script>

<style scoped>
.banner {
  display: flex;
  max-height: 500px;
  overflow: hidden;
}

.banner div {
  flex: 1;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}

#calendarImg {
  box-shadow: 0px 0px 20px black;
  -moz-box-shadow: 0px 0px 20px black;
  -webkit-box-shadow: 0px 0px 20px black;
}

#calendarImg img {
  flex-shrink: 0;
  max-height: 100%;
  max-width: 100%;
}

#calendar {
  padding: 25px;
  -ms-transform: rotate(-10deg); /* IE 9 */
  -webkit-transform: rotate(-10deg); /* Safari */
  transform: rotate(-10deg); /* Standard syntax */
}

.content {
  padding: 70px;
}
</style>

