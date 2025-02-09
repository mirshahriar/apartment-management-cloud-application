# Apartment Management Cloud Application

# Proposal for User Module Development

## Overview
This module will be part of the Apartment Management Cloud Application. It will handle user roles, authentication, and permissions, ensuring secure and efficient management of apartment projects.

## Key Features

### 1. User Roles & Access Control
- **Super Admin**
  - Manages all projects.
  - Creates new projects.
  - Adds Admins to projects.

- **Admin**
  - Manages a specific project.
  - Adds more Admins and Users.
  - Assigns roles to Users (Admin/User).
  - Marks User as Owner of the apartment.

- **User**
  - General user in a project.
  - Can be assigned as an Owner (Shareholder).

- **Owner** (Shareholder)
  - A User assigned to one or more apartments.

### 2. Authentication & Authorization
- Google login with Gmail.
- Role and permissions determined based on email after login.

### 3. Ownership & Payment History
- Admins can assign apartment ownership to the User.
- Owners can own multiple apartments in a project.
- Admins can view all owners' payment/installment histories.
- Owners can view only their own history and other owners’ basic details.

## Development Plan
- **User Authentication**: Integrate Google login and set role-based permissions.
- **Role Management**: Allow Admins to assign roles and ownership.
- **Ownership & Payments**: Develop a system to track ownership and limit access to payment data.
- **Permissions Handling**: Ensure Admins have full visibility.

## Expected Outcome
- A secure and structured apartment management system.
- Seamless Google login with role-based access.
- Scalable system to support multiple projects.

Revised Feature Breakdown

| Feature                  | Super Admin | Admin | User  | Owner |
|--------------------------|-------------|-------|-------|-------|
| **Create Projects**       | ✅          | ❌    | ❌    | ❌    |
| **Assign Roles**          | ✅          | ✅    | ❌    | ❌    |
| **View All Payment History** | ✅ | ✅    | ❌    | ❌    |
| **Edit Ownership**        | ✅          | ✅    | ❌    | ❌    |
| **View Others' Basic Info** | ✅       | ✅    | ✅**   | ✅**   |
| **Update Own Details**    | ✅          | ✅    | ✅    | ✅    |

**Notes**:  
- ✅**: Limited to viewing **name** and **unit number** of others.  
- Admins can view **full details** of all users.  
- Owners cannot edit ownership or payment data.  
