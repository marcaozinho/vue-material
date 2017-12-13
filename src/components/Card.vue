<template>
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
</template>
