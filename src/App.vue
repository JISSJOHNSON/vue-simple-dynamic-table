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
        {firstName: 'Jiss', lastName: 'Johnson', email: 'contact@jissjohnson.info', phone: '+919544497526'},
        {firstName: 'Jess', lastName: 'Johnson', email: 'contact@jessjohnson.info', phone: '+919567244423'},
        {firstName: 'Johnson', lastName: 'M Joseph', email: 'contact@johnson.info', phone: '+919895845154'},
        {
          firstName: 'Sonia',
          lastName: 'Johnson',
          email: 'contact@soniajohnson.info',
          phone: '+919895663219',
          place: 'Pambanar'
        },
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
