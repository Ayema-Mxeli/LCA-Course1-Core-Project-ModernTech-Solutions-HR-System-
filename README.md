# ModernTech HR Management System

## Student Information

**Student Name:** Ayema Mxeli
**Project:** Course 1 Core Project
**Project Title:** ModernTech HR Management System

---

## Project Overview

The **ModernTech HR Management System** is a Vue.js and Bootstrap-based single-page web application developed for **ModernTech Solutions**. The system was designed to simulate a digital HR platform that helps manage employee information, payroll, attendance, leave requests, and payslips.

This project demonstrates the use of **Vue.js components**, **reactive data handling**, **event handling**, and **localStorage** to create a responsive HR management interface without using a backend database.

---

## Features

### 1. Dashboard

The dashboard provides a quick overview of important HR information, including:

* Total number of employees
* Total leave requests
* Total attendance records

### 2. Employee Management

The system includes **15 dummy employee records** with:

* Employee ID
* Full name
* Department
* Position
* Salary

### 3. Payroll Management

The payroll section displays:

* Employee names
* Departments
* Monthly salary
* Annual salary calculation

### 4. Digital Payslip Generation

Each employee has a **View Payslip** button that displays a digital payslip showing:

* Employee name
* Department
* Position
* Monthly salary
* Annual salary
* Tax deduction
* Net salary

### 5. Leave Request Management

The leave section allows HR to:

* View leave requests
* Approve leave requests
* Deny leave requests
* See request status badges

### 6. Attendance Tracking

The attendance section displays employee attendance information, including:

* Employee name
* Department
* Attendance status
* Days present
* Days absent

### 7. localStorage Functionality

The leave request section uses **localStorage** so that approved or denied leave request statuses remain saved even after refreshing the browser.

---

## Technologies Used

* **Vue.js 3**
* **Vite**
* **Bootstrap 5**
* **HTML**
* **CSS**
* **JavaScript**

---

## Project Structure

```bash
src/
│
├── components/
│   ├── Navbar.vue
│   ├── Dashboard.vue
│   ├── EmployeeList.vue
│   ├── Payroll.vue
│   ├── LeaveRequests.vue
│   ├── Attendance.vue
│   └── Footer.vue
│
├── App.vue
└── main.js
```

---

## How to Run the Project

1. Clone the repository:

```bash
git clone https://github.com/YOUR-GITHUB-USERNAME/LCA-Course1-Core-Project.git
```

2. Open the project folder in VS Code.

3. Install dependencies:

```bash
npm install
```

4. Run the development server:

```bash
npm run dev
```

5. Open the local host link shown in the terminal.

---

## Employee Data Included

The project contains 15 dummy employee records, including employees from departments such as:

* Development
* HR
* QA
* Marketing
* Support
* Sales
* Finance

---

## Learning Outcomes Demonstrated

This project demonstrates:

* Building a single-page Vue.js application
* Creating and using Vue components
* Rendering lists with `v-for`
* Handling events with `@click`
* Conditional rendering with `v-if`
* Using reactive state with `ref()`
* Saving data in localStorage
* Styling a project using Bootstrap
* Organising a project into reusable components

---

## Future Improvements

If the project were expanded further, the following features could be added:

* Add/Edit/Delete employee forms
* Search and filter employees
* Attendance analytics charts
* Payroll export to PDF
* Authentication/login for HR admin users
* Backend database integration

---

## Conclusion

The ModernTech HR Management System successfully meets the project brief by providing a responsive HR dashboard with employee management, payroll calculations, payslip generation, leave management, and attendance tracking. The use of Vue.js, Bootstrap, and localStorage makes the project interactive, user-friendly, and suitable as a front-end HR system prototype.
