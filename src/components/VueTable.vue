/*
| ===================================================
| This File is for creating the dynamic table
| ===================================================
*/
<template>
  <div class="vue-table-container">
    <div v-if="heading">
      <h3>{{ heading }}</h3>
    </div>
    <table>
      <thead>
      <tr>
        <th v-for="(item,index) in headers" :key="index">{{ item.label }}</th>
      </tr>
      </thead>
      <tbody>
      <tr v-for="(item,index) in items" :key="index">
        <td v-for="(header,headerIndex) in headers" :key="headerIndex">{{ item[header.key] }}</td>
      </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: "VueTable",
  props: {
    heading: {
      type: String,
      required: false,
      default: null,
    },
    headers: {
      type: Array,
      required: true,
      default: () => {
        return [];
      },
    },
    items: {
      type: Array,
      required: true,
      default: () => {
        return [];
      },
    },
  },
};
</script>

<style scoped src="@/assets/style.css"></style>