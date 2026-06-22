<script setup>
import Navbar from './components/Navbar.vue'
import Dashboard from './components/Dashboard.vue'
import EmployeeList from './components/EmployeeList.vue'
import Payroll from './components/Payroll.vue'
import LeaveRequests from './components/LeaveRequests.vue'
import Attendance from './components/Attendance.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="app-bg min-vh-100">
    <Navbar />
    <Dashboard />
    <EmployeeList />
    <Payroll />
    <LeaveRequests />
    <Attendance />
      <Footer />  
  </div>
</template>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

.app-bg {
  background-color: #f8f9fa;
  padding-bottom: 40px;
}
</style>   