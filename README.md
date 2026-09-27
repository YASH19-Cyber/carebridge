# CareBridge

### Smart Clinic, Emergency & Healthcare Coordination Platform

> **Connecting Care. Coordinating Emergencies.**

CareBridge is a healthcare coordination platform designed to bring essential clinic, patient, appointment, doctor, emergency, ambulance, blood, healthcare facility, home-visit and medicine-delivery workflows into one centralized system.

The platform focuses on **coordination and administrative management**, helping patients, clinics, healthcare service providers and emergency teams manage information and requests through a unified interface.

---

## 🚀 Key Features

### 👤 Patient Management
- Patient registration and profile management
- Basic patient information
- Emergency contact details
- Blood group information
- Patient search and management

### 📅 Appointment Management
- Book appointments
- Doctor selection
- Date and time scheduling
- Appointment status tracking
- Appointment cancellation and completion
- Appointment history

### 👨‍⚕️ Doctor Directory
- Search doctors
- View doctor profiles
- Specialization information
- Availability management
- Doctor appointment booking

### 🏠 Home Doctor Visits
- Request a doctor home visit
- Track visit status
- Doctor assignment
- Visit coordination

**Workflow:**

`Requested → Accepted → Doctor Assigned → On The Way → Arrived → Visit Completed → Closed`

### 🚨 Emergency Management
- Create emergency requests
- Capture basic emergency information
- Administrative priority handling
- Emergency status tracking
- Ambulance coordination
- Emergency activity timeline

**Workflow:**

`Requested → Acknowledged → Ambulance Assigned → Dispatched → Arrived → Resolved`

### 🚑 Ambulance Coordination
- View ambulance availability
- Ambulance status management
- Dispatch ambulance
- Track assigned ambulance
- Emergency-to-ambulance coordination

### 🩸 Blood Search & Coordination
- Search by blood group
- Search by location
- View available blood units
- Create blood requests
- Coordinate blood availability

### 🏥 Healthcare Facilities
- Find nearby hospitals and clinics
- Facility information
- Location-based facility search
- Healthcare facility directory

### 💊 Medicine Delivery Coordination
- Medicine catalogue
- Pharmacy directory
- Prescription upload
- Order management
- Delivery status tracking

> CareBridge provides **service coordination only** and does not diagnose medical conditions, prescribe medicines, recommend treatments, or make medical decisions.

### 📊 Dashboard & Analytics
- Appointment statistics
- Active emergency overview
- Ambulance readiness
- Blood request overview
- Patient statistics
- Operational activity

### 🔔 Notifications
- Appointment notifications
- Emergency updates
- Ambulance status updates
- Order and service updates

### 📋 Audit & Reports
- Activity tracking
- Administrative audit logs
- CSV report export
- System activity monitoring

---

# 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │       Users         │
                    │ Patients / Staff    │
                    │ Doctors / Admins    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Web Frontend     │
                    │ HTML / CSS / JS     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    FastAPI REST     │
                    │        API          │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              ▼                ▼                ▼
        Patient Service  Appointment      Emergency
                         Service           Service
              │                │                │
              └────────────────┼────────────────┘
                               │
              ┌────────────────┼────────────────┐
              ▼                ▼                ▼
          Ambulance          Blood          Facilities
          Service           Service          Service
                               │
              ┌────────────────┼────────────────┐
              ▼                ▼                ▼
          Doctor/Home      Pharmacy        Notifications
             Visit          & Delivery
                               │
                               ▼
                    ┌─────────────────────┐
                    │    SQLAlchemy       │
                    └──────────┬──────────┘
                               │
                         ┌─────┴─────┐
                         ▼           ▼
                      SQLite     PostgreSQL
