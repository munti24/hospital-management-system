# UML Class Diagram Assignment — Hospital Management System

**Institution:** Kigali Independent University (ULK)
**Assignment:** UML Class Diagram Modelling (Released: 15 October 2026 | Deadline: 20 October 2026, 8:30 AM)
**Group:** [Student 1 Name & ID] / [Student 2 Name & ID]

## 1. Business Idea
A **Hospital Management System (HMS)** that helps a hospital manage its departments, doctors, patients,
appointments, medical records, prescriptions, rooms, and invoices in one information system.

## 2. Problem Statement
Hospitals handle large volumes of data (patients, appointments, medical records, billing). Manual or
paper-based management causes lost records, double bookings, billing errors, and slow service.
A centralised information system is needed to organise this data and model how the entities relate.

## 3. Project Scope
**Included:**
- Managing hospital departments and rooms
- Registering and managing patients
- Managing doctors and their specialisations
- Scheduling appointments between patients and doctors
- Keeping medical records per patient (diagnosis, treatment)
- Issuing prescriptions linked to appointments
- Generating invoices for patients

**Excluded:**
- Developing a fully functional application (design phase only)
- Integration with medical insurance companies
- Online pharmacy / drug inventory management

## 4. Main Classes
| Class | Responsibility |
|---|---|
| Hospital | Root of the system; contains departments; registers patients |
| Department | Groups doctors and rooms under one unit |
| Doctor | Examines patients, writes prescriptions, updates medical records |
| Patient | Registers, books appointments, receives invoices |
| Appointment | Links a patient to a doctor at a date/time |
| MedicalRecord | Stores diagnosis and treatment history of a patient |
| Prescription | Medication issued by a doctor through an appointment |
| Room | Hospital room that can be assigned to patients |
| Invoice | Bill generated for a patient |

## 5. Relationships Overview
- Hospital **contains** 1..* Departments (composition)
- Hospital **registers** * Patients (aggregation)
- Department **employs** 1..* Doctors, **has** * Rooms (composition)
- Patient **owns** exactly 1 MedicalRecord (composition)
- Patient **books** * Appointments; each Appointment is **conducted by** 1 Doctor
- Doctor **writes** * Prescriptions; an Appointment **results in** 0..1 Prescription
- Doctor **updates** * MedicalRecords
- Patient **receives** * Invoices

## 6. Repository Structure
    uml-class-diagram-assignment/
    ├── README.md
    ├── documentation/
    │   ├── report_1_project_description.pdf
    │   └── report_2_uml_class_diagram.pdf
    └── diagrams/
        ├── uml_class_diagram.drawio
        ├── uml_class_diagram.png
        └── uml_class_diagram.pdf

## 7. Tools Used
- Diagram: custom drawing exported to PNG/PDF, plus editable `.drawio` file
- Reports: PDF
