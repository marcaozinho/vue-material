<template>
    <router-view/>
</template>

<script>
export default {
  name: 'app',
  data: function() {
    return {
      contacts: []
    }
  },
  methods: {
    fillTable: function() {
      this.contacts.push({firstname: 'Marcus', lastname: 'name', email: 'aci.marcus@gmail.com'});
      this.contacts.push({firstname: 'Charles', lastname: 'name', email: 'charles@gmail.com'});
      this.contacts.push({firstname: 'Ana', lastname: 'name', email: 'ana@gmail.com'});
    },
    clearTable: function() {
      this.contacts.splice(0, this.contacts.length);
    }
  }
}
</script>

<style>
#app {
  /* font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50; */
  margin-top: 60px;
  margin-left: 30px;
  margin-right: 30px;
}
</style>
