<template>
  <div>
    <input type="text" v-model="current">
    <button @click="clear_current()">clear</button>
    <p>
      {{direction}}
    </p>
    <input type="text" v-model="destination">
    <button @click="clear_destination()">clear</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      current: '高田馬場',
      destination: "渋谷"
    }
  },
  methods: {
    clear_current () {
      this.current = ''
    },
    clear_destination () {
      this.destination = ''
    },
  },
  computed: {
        direction: function() {
            return "内回り";
        }
    }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
