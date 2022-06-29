# vue-table 

A simple dynamic table build with vue.js

### [npm](https://www.npmjs.com/package/vue-simple-dynamic-table)

## Installation

```
npm i --save vue-simple-dynamic-table
```

### Importing globally into app

```
import VueTable from 'vue-simple-dynamic-table';

Vue.use(VueTable);
```

### Importing into your component

```
import VueTable from 'vue-simple-dynamic-table';

components:{
  VueTable
}
```

### Usage

```
<template>
  <vue-table :heading="tableHeading" :headers="headers" :items="items"></vue-table>
</template>

<script>
import VueTable from 'vue-table';
...
components:{
  ...,
  VueTable
},
data(){
  return{
      headers: [
        {key: 'firstName', label: 'First Name'},
        {key: 'lastName', label: 'Last Name'},
        {key: 'email', label: 'Email'},
        {key: 'phone', label: 'Phone'},
        {key: 'place', label: 'Place'},
      ],
      items: [
        {firstName: 'John', lastName: 'Doe', email: 'john.doe@domain.com', phone: '1234567890'},
        {firstName: 'Ben', lastName: 'Mathew', email: 'ben@domain.com', phone: '1234567891'},
        {firstName: 'Alex', lastName: 'Jose', email: 'alex@domain.com', phone: '1234567892'},
      ]
  }
}
...
</script>
```

#### Author

[Jiss Johnson](https://jissjohnson.info)
