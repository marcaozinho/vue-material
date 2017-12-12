<template>
  <div id="app">
    <md-card>
      <md-card-header>
        <div class="md-title">
          Material Design With Vue.js 2 Demo
        </div>
        <div class="md-subhead">
          by Marcus Vinicius Figueiredo Meira Leite
        </div>
      </md-card-header>
      <md-card-content>
        <md-button class="md-raised md-primary" v-on:click="fillTable()">Fill Table</md-button>
        <md-button class="md-raised md-primary" v-on:click="clearTable()">Clear Table</md-button>
      </md-card-content>
      <md-table>
        <md-table-header>
          <md-table-row>
            <md-table-head>First Name</md-table-head>
            <md-table-head>Last Name</md-table-head>
            <md-table-head>Email</md-table-head>
          </md-table-row>  
        </md-table-header>
        <md-table-body>
          <md-table-row v-for="contact in contacts">
            <md-table-cell>{{ contact.firstname }}</md-table-cell>
            <md-table-cell>{{ contact.lastname }}</md-table-cell>
            <md-table-cell>{{ contact.email }}</md-table-cell>
          </md-table-row>
        </md-table-body>  
      </md-table>
    </md-card>  
    <img src="./assets/logo.png">
    <router-view/>

  </div>
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
