<template>
  <div id="app">
    <Counter personName="fred" v-on:emit-setName="logName"/>
    <div class="area">
      {{'test'}}
    </div>
    <p>{{newName}}</p>
  </div>
</template>

<script>
import Counter from './components/Countainer'

export default {
  name: 'app',
  components: {
    Counter
  },
  data() {
    return {
      newName: '__'
    }
  },
  methods: {
    logName(e) {
      console.log('e', e)
      this.newName = e
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.area {
  padding-top: 30px
}
</style>
