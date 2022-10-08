<template>
  <div id="app">
    <h2>Vue Get Current Date</h2>
    Current Date: {{ currentDate() }}
    <br/>
    Current Date Time: {{ currentDateTime() }}
  </div>
   
</template>

<script>

export default {
  name: 'App',
  methods: {
    currentDate() {
      const current = new Date();
      const date = `${current.getDate()}/${current.getMonth()+1}/${current.getFullYear()}`;
      return date;
    },
    currentDateTime() {
      const current = new Date();
      const date = current.getFullYear()+'-'+(current.getMonth()+1)+'-'+current.getDate();
      const time = current.getHours() + ":" + current.getMinutes() + ":" + current.getSeconds();
      const dateTime = date +' '+ time;

      return dateTime;
    }
  }
}
</script>
<style>
#app {
  position: fixed;
    top: 30%;
    left: 20%;
    font-size: 2rem;
    font-weight: bold;
}
</style>
