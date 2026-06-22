<template>
  <div class="container mt-5">
    <h2>Leave Requests</h2>

    <table class="table table-hover mt-3">
      <thead class="table-dark">
        <tr>
          <th>Employee Name</th>
          <th>Leave Type</th>
          <th>Days</th>
          <th>Status</th>
          <th>Actions</th>
        </tr>
      </thead>

      <tbody>
        <tr v-for="request in leaveRequests" :key="request.id">
          <td>{{ request.name }}</td>
          <td>{{ request.type }}</td>
          <td>{{ request.days }}</td>
          <td>
            <span
              class="badge"
              :class="{
                'bg-warning text-dark': request.status === 'Pending',
                'bg-success': request.status === 'Approved',
                'bg-danger': request.status === 'Denied'
              }"
            >
              {{ request.status }}
            </span>
          </td>
          <td>
            <button
              class="btn btn-success btn-sm me-2"
              @click="approveRequest(request.id)"
              :disabled="request.status !== 'Pending'"
            >
              Approve
            </button>

            <button
              class="btn btn-danger btn-sm"
              @click="denyRequest(request.id)"
              :disabled="request.status !== 'Pending'"
            >
              Deny
            </button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup>
import { ref, onMounted, watch } from 'vue'

const defaultLeaveRequests = [
  { id: 1, name: 'Mimi Ngulube', type: 'Annual Leave', days: 3, status: 'Pending' },
  { id: 2, name: 'Avela James', type: 'Sick Leave', days: 4, status: 'Approved' },
  { id: 3, name: 'Bianca Yengwa', type: 'Family Responsibility Leave', days: 2, status: 'Approved' },
  { id: 4, name: 'Akhile Kumar', type: 'Annual Leave', days: 5, status: 'Pending' },
  { id: 5, name: 'Naledi Manentsa', type: 'Sick Leave', days: 2, status: 'Denied' }
]

const leaveRequests = ref([])

onMounted(() => {
  const savedRequests = localStorage.getItem('leaveRequests')
  if (savedRequests) {
    leaveRequests.value = JSON.parse(savedRequests)
  } else {
    leaveRequests.value = defaultLeaveRequests
  }
})

watch(
  leaveRequests,
  (newValue) => {
    localStorage.setItem('leaveRequests', JSON.stringify(newValue))
  },
  { deep: true }
)

const approveRequest = (id) => {
  const request = leaveRequests.value.find(req => req.id === id)
  if (request) {
    request.status = 'Approved'
  }
}

const denyRequest = (id) => {
  const request = leaveRequests.value.find(req => req.id === id)
  if (request) {
    request.status = 'Denied'
  }
}
</script>     
