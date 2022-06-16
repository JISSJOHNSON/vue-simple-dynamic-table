<template>
  <div id="app">
    <VueTable heading="Users" :headers="headers" :items="items"></VueTable>
  </div>
</template>

<script>
import VueTable from "@/components/VueTable";

export default {
  name: 'App',
  components: {
    VueTable
  },
  data() {
    return {
      headers: [
        {key: 'firstName', label: 'First Name'},
        {key: 'lastName', label: 'Last Name'},
        {key: 'email', label: 'Email'},
        {key: 'phone', label: 'Phone'},
        {key: 'place', label: 'Place'},
      ],
      items: [
        {firstName: 'John', lastName: 'Doe', email: 'john@domain.com', phone: '1234567891'},
        {firstName: 'Ben', lastName: 'Tiago', email: 'ben@domain.com', phone: '1234567892'},
        {firstName: 'Alex', lastName: 'Joseph', email: 'alex@domain.com', phone: '1234567893'},
      ]
    };
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
