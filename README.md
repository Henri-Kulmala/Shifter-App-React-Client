# Shifter – React Admin Client

Shifter is a React-based admin control panel for managing work shifts, employees, and schedules in a retail environment.  
The application was developed as part of a university course and designed around a real workplace use case in grocery retail.

This frontend communicates with a separate Java Spring Boot backend via REST APIs and is intended for internal managerial use rather than public access.

---

## Purpose & Use Case

The frontend application is designed for store managers to:
- Plan daily work shifts
- Assign employees to shifts and workstations
- Define working hours and breaks
- Manage employees and user accounts
- View saved workdays
- Export workday schedules as PDF files for sharing

The application models a real internal planning tool rather than a consumer-facing product.

---

## Tech Stack

- React
- TypeScript
- Vite
- REST API integration
- CSS Modules

---

## Authentication & Roles

- Session-based authentication handled by backend
- Login via form-based authentication
- Role-based access control
- Users have either `ADMIN` or `USER` privileges
- Most management functionality is restricted to `ADMIN` users

---

## Application Pages

### Login
Authentication view with validation and error handling.

<details open>
<summary>Preview</summary>

![Login page](https://github.com/user-attachments/assets/3c108112-d826-47a8-8cb4-968e636066af)

![Login error](https://github.com/user-attachments/assets/f93cd54d-be3b-4dfc-bebc-739bfdcebce7)
</details>

---

### Landing Page
Initial view after successful authentication.

<details open>
<summary>Preview</summary>

![Landing page](https://github.com/user-attachments/assets/79c035c0-68a7-4672-bb75-ae55475b5a09)
</details>

---

### ShiftPlanner
Primary planning interface for creating and editing workdays.

Features:
- Select a date from a calendar
- Automatically generate default shifts
- Edit shift name, time, workstation, and breaks
- Assign employees to shifts
- Save workday data to backend

Supports minimized and expanded views for improved usability.

<details open>
<summary>Minimized view</summary>

![Minimized ShiftPlanner](https://github.com/user-attachments/assets/5e69a21e-78ab-43a6-b61c-4b13f1106577)
</details>

<details open>
<summary>Expanded view</summary>

![Expanded ShiftPlanner](https://github.com/user-attachments/assets/f4c67c18-a0fb-4ef7-8519-bc12caf535c6)
</details>

---

### Schedule
View previously saved workdays and export schedules.

Features:
- Calendar-based date selection
- Viewing stored workdays
- Exporting workday data as PDF files

<details open>
<summary>Preview</summary>

![Schedule view](https://github.com/user-attachments/assets/182206a1-242f-48c8-8903-5745ca4c77cb)
</details>

---

### Profile / Account Management
Manage users and employee data.

Features:
- Create, edit, and delete users
- Assign roles (ADMIN / USER)
- Password validation
- Confirmation dialogs for destructive actions

<details>
<summary>Preview</summary>

![Profile page](https://github.com/user-attachments/assets/c346cf29-f7a4-4635-85b1-05dc8f2ffc30)

![User list](https://github.com/user-attachments/assets/94ed332c-b4ae-4603-b708-f19031cecc89)

![Edit user](https://github.com/user-attachments/assets/53e0869a-0e04-4b52-9fd5-c153c2b88f20)

![Delete confirmation](https://github.com/user-attachments/assets/c690b1b3-bb01-4f3e-a874-f17e03215405)

![Password validation](https://github.com/user-attachments/assets/14960434-d2d2-410f-b0f6-7aa79e570bc8)

![Password validation error](https://github.com/user-attachments/assets/2cef1617-b309-4652-824d-97f18232e703)
</details>

---

## Project Structure

The project follows a standard Vite + React structure:
- Page-based routing
- Reusable UI components
- API communication layer
- CSS Modules for scoped styling

---

## Local Development

### Requirements
- Node.js
- npm or yarn
- Running backend server

### Install dependencies
```bash
npm install
````

### Start development server
```bash
npm run dev
````

### Environment Variables
The frontend expects environment variables such as:
```bash
VITE_API_URL=http://localhost:8080
````
These variables define the backend API base URL.

---

## Backend Dependency

This frontend requires the Shifter backend to be running locally.
All authentication, authorization, data persistence, and business logic are handled by the backend service.

Backend repository:


[Shifter Backend](https://github.com/Henri-Kulmala/Shifter--Vuoronsuunnittelu)

---

## Project Status

This project was developed for educational and portfolio purposes.
While designed around a real workplace use case, it is not actively maintained for production deployment.
