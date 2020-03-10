<template>
  <div id="app">
    <h1>Employees</h1>
    <employee-table :employees="employees" />
  </div>
</template>

<script>
  import EmployeeTable from "@/components/EmployeeTable.vue"
  export default {
    name: 'App',
    components: {
      EmployeeTable
    },
    data() {
      return {
        employees: [{
            id: 1,
            name: 'Omotola Olajide',
            social: 'facebook',
          },
          {
            id: 2,
            name: 'Omotola Olajide',
            social: 'twitter',
          },
          {
            id: 3,
            name: 'Omotola Olajide',
            social: 'instagram',
          },
        ],
      }
    },
  }
</script>

<style>
  button {
    background: #009435;
    border: 1px solid #009435;
  }

  .small-container {
    max-width: 680px;
  }
</style>