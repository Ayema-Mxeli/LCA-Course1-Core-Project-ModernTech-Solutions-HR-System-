<template>
  <div class="container mt-5">
    <h2>Employees</h2>

    <table class="table table-striped mt-3">
      <thead>
        <tr>
          <th>ID</th>
          <th>Name</th>
          <th>Department</th>
          <th>Position</th>
          <th>Salary</th>
        </tr>
      </thead>

      <tbody>
        <tr v-for="employee in employees" :key="employee.id">
          <td>{{ employee.id }}</td>
          <td>{{ employee.name }}</td>
          <td>{{ employee.department }}</td>
          <td>{{ employee.position }}</td>
          <td>R{{ employee.salary }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const employees = ref([
  { id: 1, name: 'Iva James', department: 'Development', position: 'Frontend Developer', salary: 35000 },
  { id: 2, name: 'Bianca Yengwa', department: 'HR', position: 'HR Manager', salary: 32000 },
  { id: 3, name: 'Elam Willians', department: 'QA', position: 'QA Tester', salary: 28000 },
  { id: 4, name: 'Lisa Johns', department: 'Marketing', position: 'Marketing Specialist', salary: 30000 },
  { id: 5, name: 'Qhayiya Mxeli', department: 'Support', position: 'Support Agent', salary: 22000 },
  { id: 6, name: 'Naledi Manentsa', department: 'Development', position: 'Backend Developer', salary: 38000 },
  { id: 7, name: 'Mimi Ngulube', department: 'Sales', position: 'Sales Executive', salary: 27000 },
  { id: 8, name: 'Sophia Hendrix', department: 'HR', position: 'Recruiter', salary: 26000 },
  { id: 9, name: 'Angelista Ndlovu', department: 'QA', position: 'QA Analyst', salary: 29000 },
  { id: 10, name: 'Akhile Kumar', department: 'Marketing', position: 'Content Creator', salary: 25000 },
  { id: 11, name: 'Siyolise Nkosi', department: 'Development', position: 'Full Stack Developer', salary: 42000 },
  { id: 12, name: 'Avela James', department: 'Support', position: 'Support Lead', salary: 26000 },
  { id: 13, name: 'Lihle Mthembu', department: 'Sales', position: 'Sales Manager', salary: 34000 },
  { id: 14, name: 'Ayanda Titi', department: 'Finance', position: 'Payroll Officer', salary: 31000 },
  { id: 15, name: 'Alizwa Paul', department: 'Development', position: 'UI Designer', salary: 33000 }
])
</script> 