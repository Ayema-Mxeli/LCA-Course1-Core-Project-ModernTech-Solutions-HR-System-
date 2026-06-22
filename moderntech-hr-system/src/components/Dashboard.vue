<template>
  <div class="container mt-4">
    <h2>Dashboard</h2>

    <div class="row mt-3">
      <div class="col-md-4 mb-3">
        <div class="card text-center shadow-sm">
          <div class="card-body">
            <h5>Total Employees</h5>
            <h3>{{ totalEmployees }}</h3>
          </div>
        </div>
      </div>

      <div class="col-md-4 mb-3">
        <div class="card text-center shadow-sm">
          <div class="card-body">
            <h5>Leave Requests</h5>
            <h3>{{ totalLeaveRequests }}</h3>
          </div>
        </div>
      </div>

      <div class="col-md-4 mb-3">
        <div class="card text-center shadow-sm">
          <div class="card-body">
            <h5>Attendance Records</h5>
            <h3>{{ totalAttendanceRecords }}</h3>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const totalEmployees = 15
const totalLeaveRequests = 5
const totalAttendanceRecords = 6
</script> 