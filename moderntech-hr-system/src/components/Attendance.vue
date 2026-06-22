<template>
  <div class="container mt-5">
    <h2>Attendance Tracking</h2>

    <table class="table table-striped mt-3">
      <thead class="table-dark">
        <tr>
          <th>Employee Name</th>
          <th>Department</th>
          <th>Status</th>
          <th>Days Present</th>
          <th>Days Absent</th>
        </tr>
      </thead>

      <tbody>
        <tr v-for="employee in attendanceRecords" :key="employee.id">
          <td>{{ employee.name }}</td>
          <td>{{ employee.department }}</td>
          <td>
            <span
              class="badge"
              :class="{
                'bg-success': employee.status === 'Present',
                'bg-danger': employee.status === 'Absent',
                'bg-warning text-dark': employee.status === 'On Leave'
              }"
            >
              {{ employee.status }}
            </span>
          </td>
          <td>{{ employee.presentDays }}</td>
          <td>{{ employee.absentDays }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const attendanceRecords = ref([
  { id: 1, name: 'Lisa Johns', department: 'Marketing', status: 'Present', presentDays: 20, absentDays: 4 },
  { id: 2, name: 'Bianca Yengwa', department: 'HR', status: 'On Leave', presentDays: 18, absentDays: 2 },
  { id: 3, name: 'Akhile Kumar', department: 'Marketing', status: 'Present', presentDays: 21, absentDays: 0 },
  { id: 4, name: 'Avela James', department: 'Support', status: 'Absent', presentDays: 17, absentDays: 4 },
  { id: 5, name: 'Ayanda Titi', department: 'Finance', status: 'Present', presentDays: 22, absentDays: 0 },
  { id: 6, name: 'Elam Willians', department: 'QA', status: 'Present', presentDays: 19, absentDays: 1 }
])
</script> 