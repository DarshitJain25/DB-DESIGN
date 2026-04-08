# DB-DESIGN
# Clinic Appointment and Diagnostics Platform

I have completed the task of designing the db scheme for a Clinic Appointment and Diagnostics Platform

I have taken : 
// Tables 

1. patient
2. doctors
3. reports
4. appointments
5. consultations
6. doctorspecializations
7. tests

   
// relations 

patient.patient_id < appointments.patient_id [1 : Many]


// a doctor can have many specializations 
doctors.doctor_id < doctorspecializations.doctor_id  [1 : Many]


// multiple tests for single consultation 
tests.appointment_id > consultation.appointment_id [Many : one]


// multiple reports for a single patient
reports.patient_id > patient.patient_id   [Many : one]


// one doctor can have different appointments
doctors.doctor_id  < appointments.doctor_id   [1 : Many]


// one specific test result in sepcific report
tests.test_id  - reports.test_id  [1 : one]
