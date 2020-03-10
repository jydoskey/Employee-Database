<template>
  <div id="app">
    <h1>Employees</h1>
    <employee-form @add:employee="addEmployee" />
    <employee-table :employees="employees" />
  </div>
</template>

<script>
  import EmployeeForm from "@/components/EmployeeForm.vue"
  import EmployeeTable from "@/components/EmployeeTable.vue"
  export default {
    name: 'App',
    components: {
      EmployeeTable,
      EmployeeForm,
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
    methods: {
      addEmployee(employee) {
        const lastId = 
          this.employees.length > 0
            ? this.employees[this.employees.length - 1].id
            : 0;
        const id = lastId + 1;
        const newEmployee = {...employee, id};
        this.employees = [...this.employees, newEmployee];
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