# NGHFM Enterprise Management Portal

## Overview

NGHFM (Nidhi Group Hospitality & Facility Management) is an enterprise workforce and operations management platform built for organizations operating across multiple branches and sites.

The system centralizes employee management, attendance tracking, payroll processing, shift scheduling, geofencing, asset management, client management, and document management under a unified role-based access control architecture.

The platform supports multi-location operations where data visibility and access are automatically restricted based on the user's assigned branch location.

---

## Technology Stack

### Backend

* Laravel 12
* PHP 8.2+
* Laravel Fortify
* Laravel Sanctum
* Spatie Laravel Permission
* Inertia.js

### Frontend

* React
* TypeScript
* Tailwind CSS
* Inertia.js

### Database

* MySQL

### Maps & Location Services

* Leaflet Maps
* GeoIP Integration
* Geofencing Engine

---

## Core Features

### Authentication & Security

* Secure Login System
* Laravel Fortify Authentication
* Two-Factor Authentication
* Sanctum API Authentication
* Session Management
* Password Encryption
* Protected Route Middleware

---

### Role Based Access Control (RBAC)

Implemented using Spatie Laravel Permission.

#### Roles

* Super Admin
* HR
* Site Manager
* Accountant
* Field Staff

#### Permission-Based Modules

* Attendance Management
* Payroll Management
* Leave Management
* Geofencing
* Reports
* Assets
* Documents
* Scheduling

Users can have one or multiple roles and permissions can be assigned independently.

---

## Multi-Location Data Isolation

The platform supports multiple branch locations.

### Location Architecture

Each user is assigned:

* current_location_id
* site_id

Global scopes automatically filter records based on the currently selected location.

### Benefits

* Branch-wise data separation
* Controlled visibility
* Shared platform infrastructure
* Centralized administration

---

## Modules

### Dashboard

Provides operational overview including:

* Active Employees
* Attendance Statistics
* Payroll Summary
* Shift Overview
* Site Coverage Metrics

---

### User Management

Features:

* Employee Creation
* Profile Management
* Role Assignment
* Document Verification
* Site Assignment
* Branch Assignment
* User Activation / Deactivation

---

### Shift Scheduling System

Supports:

#### Single Employee Assignment

Assign shift to one employee.

#### Bulk Assignment

Assign shifts to multiple employees simultaneously.

#### Role-Based Assignment

Assign shifts to all employees under a selected role.

Features:

* Shift Type Management
* Site Assignment
* Date & Time Scheduling
* Notes & Instructions

---

### Attendance Management

Features:

* Employee Attendance Tracking
* Attendance Filtering
* Check-In / Check-Out Records
* Attendance Verification
* Anomaly Detection
* Role-Based Visibility

---

### Payroll Management

Features:

* Monthly Payroll Generation
* Attendance-Based Salary Processing
* Overtime Calculation
* Salary Slip Generation
* PF Reports
* ESIC Reports
* Bank Export Reports
* Approval Workflow

---

### Leave Management

Features:

* Leave Requests
* Leave Approval Workflow
* Leave Balance Tracking
* Leave History
* Status Management

---

### Site Management

Features:

* Site Creation
* Site Code Generation
* Employee Assignment
* Role-Based Assignment
* Geofence Configuration

Supports:

* Circle Geofence
* Polygon Geofence
* Rectangle Geofence

---

### Geofencing System

Built using interactive maps.

Features:

* Geofence Creation
* Radius Configuration
* Site Linking
* Employee Assignment
* Location Validation

Supported Shapes:

* Circle
* Polygon
* Rectangle

---

### Client Management

Features:

* Client Registration
* Site Mapping
* Contact Information Management
* Status Tracking

---

### Asset Management

Features:

* Asset Registration
* Asset Assignment
* Warranty Tracking
* Asset Categories
* Asset Status Tracking
* Site-Based Asset Allocation

---

### Document Management

Features:

* Employee Documents
* Verification Workflow
* Approval / Rejection
* Secure Storage
* Controlled Access

---

### Notifications

Features:

* System Notifications
* User Notifications
* Administrative Announcements

---

### Inventory Management

Features:

* Branch-Level Inventory Tracking
* Centralized Inventory Overview
* Asset Integration

---

## Architecture Highlights

### Global Scope Based Data Isolation

Custom scopes:

* LocationScope
* SiteScope

Automatically restrict data visibility based on:

* User Location
* User Site

---

### Custom Traits

#### BelongsToLocation

Provides:

* Automatic location assignment
* Global location filtering

#### BelongsToSite

Provides:

* Automatic site assignment
* Site-level filtering

---

## Database Relationships

Key entities:

* Users
* Roles
* Permissions
* Locations
* Sites
* Geofences
* Attendance
* Payroll
* Salary Slips
* Leave Requests
* Assets
* Clients
* Documents
* Notifications

---

## Security Features

* Role-Based Authorization
* Permission-Based Authorization
* Middleware Protection
* Global Data Scoping
* Two-Factor Authentication
* Secure Password Hashing
* Sanctum Authentication

---

## Business Benefits

* Centralized Workforce Management
* Multi-Branch Operations Support
* Payroll Automation
* Attendance Automation
* Geofence-Based Workforce Monitoring
* Permission-Controlled Access
* Operational Transparency
* Reduced Administrative Overhead

---

## Future Enhancements

* Face Recognition Attendance
* GPS Spoof Detection
* Real-Time Employee Tracking
* Advanced Analytics Dashboard
* AI-Based Workforce Insights
* Multi-Tenant SaaS Architecture

---

## Author

Developed using Laravel, React, TypeScript, Inertia.js, MySQL, Spatie Permission, Sanctum, and Enterprise RBAC Architecture.
