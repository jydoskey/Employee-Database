<template>
  <div id="employee-form">
    <form>
      <label>Employee name</label>
      <input v-model="employee.name" type="text" />
      <label>Employee Social</label>
      <input v-model="employee.social" type="text">
      <button>Add Employee</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'employee-form',
  data() {
    return {
      employee: {
        name: '',
        social: '',
      },
    }
  },
}
</script>

<style lang="scss" scoped>
  form {
    margin-bottom: 2rem;
  }
</style>