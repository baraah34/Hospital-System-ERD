primary key:
Patient: PatientID
Medical Record: RecordID
Appointment: AppointmentID
Doctor: DoctorID
Department: DepartmentID
Service: ServiceID
Billing: BillingID
Insurance: InsuranceID
 Relation:
Patient - Appointment	1:M	One patient can book many appointments
Doctor - Appointment	1:M	One doctor handles many appointments
Doctor - Department	M:1	Many doctors work in one department
Patient - Medical Record	1:M	One patient can have multiple medical records over time
Appointment - Service	M:1	Multiple appointments might include the same type of service
Patient - Billing	1:M	One patient can have multiple bills
Insurance - Billing	1:M	One insurance provider can generate many bills
Department - Doctor	1:1	(Manage) One doctor manages one department

Participation:
Total Participation :
Medical Record: A medical record must belong to a Patient (v "Has A") and must be written by a Doctor (v "Writes").
Appointment: appointment must be linked to a Patient and a Doctor.
Billing: A bill must be associated with a Patient.

Partial Participation :
Insurance: Not every patient may have insurance, and not every bill is necessarily covered by insurance.
Doctor (Manage): Not every doctor is a manager of a department.
Patient: patient exists in the system even if they haven't booked an appointment yet.
