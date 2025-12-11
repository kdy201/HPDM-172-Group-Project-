# HPDM172 Hospital Database Project

This repository contains the group project for the **HPDM172 – Computational Skills for Health and Life Sciences** module.  
The aim of this project is to design, build, and query a realistic **hospital information system database** using MySQL.  
The database includes several tables, including; hospitals, doctors, patients, prescriptions, diseases, medications, appointments, and lab results.

The project includes:
- Entity Relationship Diagrams (ERDs)
- SQL table creation scripts
- Required SQL queries (1–19)
- A teamwork portfolio

---

# 🏥 Database Overview

The database models a complete hospital information management system with the following core tables:

### **Hospitals**
- hospital_id (PK)
- hospital_name 
- hospital_address
- num_beds
- hospital_type
- hospital_accreditation_status
- established_date
- emergency_service
- accreditation_date 

### **Doctors**
- doctor_id
- doctor_name
- doctor_dob
- doctor_address
- hospital_id


### **Patients**
- patient_id
- patient_name
- patient_dob
- patient_address
- doctor_id


### **Medications**
- medication_id (PK)
- medication_name


### **Prescriptions**
- prescription_id
- patient_id
- doctor_id
- date_prescribed
- hospital_id
- medication_id


### **Diseases**
- disease_id
- disease_name

### **Disease_Medication** 
- medication_id
- disease_id

### **Specialist**
- doctor_id
- disease_id
- hospital_id

### **Appointments**
- appointment_id
- patient_id
- doctor_id
- hospital_id
- appointment_date
- appointment_time
- appointment_type



### **LabResults**
- lab_result_id
- patient_id
- doctor_id
- hospital_id
- test_name
- result_value
- result_unit
- result_flag
- result_date


---

# SQL Queries

Each SQL file in the `/queries` folder corresponds to a required task.

### Query 1 — Doctors working at a specific hospital
Lists all doctors assigned to a chosen hospital.

### Query 2 — All prescriptions for a particular patient ordered by the prescription date
Shows all prescriptions ordered by most recent.

### Query 3 — All prescriptions prescribed by a particular doctor
Displays all prescriptions written by a specific doctor.

### Query 4 — All prescriptions ordered alphabetically by patient name
Outputs an alphabetically sorted prescription list.

### Query 5 — Add a new patient & register them with a doctor
Demonstrates INSERT commands with foreign keys.

### Query 6 — Modify an existing patient’s address
Updates the address of a selected patient.

### Query 7 — Patients registered to doctors at a particular hospital
Used for administrative or mailing list purposes.

### Query 8 — Doctors at teaching hospitals accredited 2015–2024
Filters by hospital type and accreditation year.

### Query 9 — Patients who may have a particular disease
Identifies patients based on medications linked to diseases.

### Query 10 — Doctors specialising in a specific disease
Finds specialists based on disease mappings.

### Query 11 — Lab results for all patients over age 60
Uses joins and age filtering.

### Query 12 — All appointments for a given patient
Retrieves appointment history.

### Query 13 — All appointments for a given doctor
Shows all appointments for one doctor.

### Query 14 — Prescriptions from a specific hospital
Outputs:
- medication name  
- doctor name  
- patient name  
- hospital name  

### Query 15 — Lab results from hospitals accredited 2013–2020
Filters lab results using accreditation criteria.

### Query 16 — Doctor with the most prescriptions
Uses COUNT and GROUP BY.

### Query 17 — Doctors at the largest hospital
Finds doctors working at the hospital with the most beds.

### Query 18 — Hospitals accredited before 2015 with emergency services
Filters by accreditation year and emergency availability.

### Query 19 — Patients registered with doctors at hospitals < 400 beds
Uses multi-table join filtering.


# ▶️ How to Use the Files

### **STEP 0 - Open Linux and 
#FIX THIS 

### **STEP 1 — Create the Database and Tables**
#fix thos 

### **STEP 2 — Create the Tables**

Run all required CREATE TABLE statements for your tables  
(Hospitals, Doctors, Patients, Appointments, LabResults, Medications, etc.)

These definitions are included in the project documentation.
Th


### **STEP 4 — Run SQL Queries from the /queries folder**

Example:

mysql -u root -p hospital_db < queries/query_appointments_by_patient.sql


### **STEP 5 — Export the Final Database**

Use mysqldump to generate the final project export file:

mysqldump -u root -p hospital_db > database/hospital_db_export.sql
