# Group-Project-1
Group 1: 
Group Members: 
Caroline 
Gwen --> https://github.com/gaw63800/GroupProjectMIST4610-Group1![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/bba2c5ca-bb78-4a92-b2b6-61b249d05327)
Charlie --> https://github.com/charles8888/Project-1 ![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/ebcc4367-dcdc-401e-949c-23b1ea738bd8)

Hubah --> https://github.com/hubahakhtar/Project1![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/e9709fb9-159d-4fdc-9282-5dc09c61e32e)

Kishen --> https://github.com/supersomeone03/Project-1![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/295edf8e-2770-4e3a-935a-ad0efadba154)


Problem Description: 
Pretend you are the owner/operator of an emergency healthcare clinic needing to build a relational database. You hired some students from the MIST 4610 class at the University of Georgia to create the database for you. They need to know more about your organization to identify which entities, attributes, and relationships are important for you. Start by describing your business as a real client!

Chat GPT Conversation: 
You
Hi. I am the owner of an emergency healthcare clinic needing to build a relational database. I hired some students from the MIST 4610 class at the University of Georgia to create the database for my business. I need to know more about your organization to identify which entities, attributes, and relationships are important for this business data model
ChatGPT
Sure, I'd be happy to help you identify important entities, attributes, and relationships for your emergency healthcare clinic database. To better assist you, could you provide more details about your organization and the specific functionalities you'd like to include in the database? For example:
1.	What are the primary services offered by your emergency healthcare clinic? (e.g., urgent care, primary care, specialized care)
2.	What types of healthcare professionals do you employ? (e.g., doctors, nurses, physician assistants)
3.	What patient information do you need to store? (e.g., demographic information, medical history)
4.	What types of medical equipment or resources do you need to manage? (e.g., medical supplies, medications, equipment maintenance)
5.	Do you have any specific reporting or analytics requirements? (e.g., tracking patient outcomes, monitoring clinic performance)
Once I have a better understanding of your organization's needs, I can help identify relevant entities, attributes, and relationships for your database.
You
What do you think our needs should be as an emergency healthcare clinic?
ChatGPT
As an emergency healthcare clinic, your primary focus is on providing rapid and effective care to patients who require immediate medical attention. Based on this focus, here are some essential needs that your database should address:
1.	Patient:
•	Entities: Patients
•	Attributes: Name, address, contact information, date of birth, insurance information, medical history, allergies, emergency contacts.
•	Relationships: Patients may have multiple visits or encounters. Each visit can have details such as date, time, reason for visit, attending healthcare provider, diagnosis, treatment provided, and discharge information.
2.	Staff:
•	Entities: Doctors, nurses, physician assistants, etc.)
•	Attributes: Name, contact information, role/title, qualifications, work schedule.
•	Relationships: Staff members may have different roles, shifts, and responsibilities. Assignments to patient cases or visits should also be tracked.
3.	Inventory:
•	Entities: Medical equipment, supplies, medications.
•	Attributes: Item name, description, quantity on hand, expiration date (for medications and perishable supplies), supplier information, cost.
•	Relationships: Track usage of items, restocking, and inventory levels.
4.	Billing and Insurance:
•	Entities: Invoices, insurance companies.
•	Attributes: Invoice number, patient details, services provided, charges, insurance policy details.
•	Relationships: Link patient visits to billing information. Track payments, outstanding balances, and insurance claims.
5.	Emergency Room Operations:
•	Entities: Rooms, beds, triage information.
•	Attributes: Room/bed number, availability, triage level.
•	Relationships: Assign patients to available rooms or beds. Track waiting times and prioritize patients based on urgency.
6.	Quality Assurance and Reporting:
•	Entities: Quality metrics, incident reports.
•	Attributes: Type of incident, date/time, involved parties, severity, resolution.
•	Relationships: Link incidents to patient encounters for follow-up and improvement initiatives. Generate reports on patient outcomes, wait times, and clinic performance.
These are just some initial considerations based on the typical needs of an emergency healthcare clinic. Depending on the specific requirements of your clinic, you may need to further customize the database schema and functionalities.

Data Model:
<img width="524" alt="image" src="https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/ce14e66b-445a-45e9-822c-949a1777c13a">

Data Dictionary: 
Table: Appointment
Col. Name	Description	Data Type	Size	Format	Key?
appointmentID	Unique sequential number indicating the identification number of the appointment	int	5		PK
Date	Date of the specific appointment	Date	10		
Appointmentcol*	Optional additional appointment notes	Varchar(45)	45		
patient_patientID	Unique sequential number indicating the identification number of the corresponding patient with the appointment	int	3		PK
Staff_staffID	Unique sequential number indicating the identification number of the corresponding staff member for the appointment	int	4		PK
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/54326659-0250-4a53-997d-69c4e6b1189c)

 Table: Emergency_Contact
Col. Name	Description	Data Type	Size	Format	Key?
EC_ID	Unique sequential number indicating the identification number of the specific instance of an emergency contact	int	2-4		PK
EC_Phone	Phone number of each emergency contact	Varchar(45)	12		
EC_Address	Address of each emergency contact	Varchar(45)	45		
EC_Other	Additional Info (optional)	Varchar(45)	45		
patient_patientID	Unique sequential number indicating the identification number of the corresponding patient 	int	3		PK
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/59ed8053-8f66-4a18-b731-846c00f90814)

Table: Equiqment (Note: should have been EQUIPMENT—TYPO)
Col. Name	Description	Data Type	Size	Format	Key?
Equiqment_ID	Unique sequential number indicating the identification number of equipment	int	4		PK
Type	Name of the type of equipment	Varchar(45)	45		
Description	Optional text description of equipment	Varchar(45)	45		
Quantity	Quantity of type of equiptment	int	1-2		
Expiration_Date	Expiration date of equiptment	Date	10		
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/b084e5af-3e33-4596-83d1-6ab3db9a4937)

Table: Invoice
Col. Name	Description	Data Type	Size	Format	Key?
InvoiceNum	Unique sequential number indicating the identification number of each invoice	Int	4-6		PK
days_of_Stay	Number of days of stay	Int	2-3		
Balence_Due	Monetary balance due	Int	4-5		
Note: TYPO (meant Balance_Due)
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/197d8bab-6ca2-4533-93f2-26940fd7ebcb)

Table: patient
Col. Name	Description	Data Type	Size	Format	Key?
patientID	Unique sequential number indicating the identification number of each patient	int	1-4		PK
patient_Name	Name of patient	Varchar(45)	45		
patient_address	Address of patient	Varchar(45)	45		
patient_contact	Email address of patient for contact	Varchar(45)	45		
date of birth	DOB of patient	Date	10		
insuranceID	Patient insurance ID	int	7		
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/f61e250c-397c-4282-8e66-39d94f76c434)

Table: patient_has_Invoice
Col. Name	Description	Data Type	Size	Format	Key?
patient_patientID	Unique sequential number indicating the identification number of each patient	int	1-4		PK
Invoice_InvoiceNum	Unique sequential number indicating the identification number of each invoice	int	4-6		PK
Charge	Name of the charge type/purpose	Varchar(45)	45		
Desc	Optional additional description of charge	Varchar(45)	45		
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/8194b6a3-3d2a-4dcb-b502-04262bcf6930)


Table: Payroll
Col. Name	Description	Data Type	Size	Format	Key?
CheckNum	Unique sequential number indicating the identification number of each check	int	1-5		PK
DATE	Date which each check is filled out	Date	10		
Amount	Amount which check is for	int	3-4		
Hours_worked	Hours worked per the check	int	1-2		
Hourly_Rate	Hourly rate of the staff which the check is for	int	2-4		
Staff_staffID	Unique sequential number indicating the identification number of the corresponding staff member for the appointment	int	4		PK
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/53bfab53-f04d-4d0c-b1e4-63c7c02bc0fd)

Table: Procedures
Col. Name	Description	Data Type	Size	Format	Key?

Name	Name of procedure	varchar(45)
	45		PK
Length	Amount of time spent on procedure	varchar(45)
	45		
Desc	Optional additional description of procedure	varchar(45)
	45		
Appointment_appointmentID	Represents the unique identifier for an appointment	int	5		PK
Appointment_patient_patientID	Represents the unique identifier for a patient associated with an appointment	int	2-3		PK

Appointment_Staff_staffID	Represents the unique identifier for a staff member associated with an appointment.	int	4		PK

![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/a2237bb1-2005-4546-8588-774028b94cc5)


Table: Review
Col. Name	Description	Data Type	Size	Format	Key?

reviewNum	Represents the unique identifier for a review.	int 
	2-5		PK
Date
	Represents the date when the review was submitted.	date
	10		
Desc
	Represents the description or content of the review.	varchar(45)
	45		
Rating
	Represents the rating given in the review, indicating the level of satisfaction or performance.	varchar(45)
	45		
patient_patientID	Represents the unique identifier for a patient associated with the review.	int	2-3		PK
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/53189685-18fe-47ed-9231-fdc3f85234d0)

Table: Rooms
Col. Name	Description	Data Type	Size	Format	Key?

roomNum	Represents the room number in a medical facility.	int 
	1-5		PK
bedCount
	Indicates the total number of beds available in the room.	varchar(45)
	45		
availabilty
	Represents the current availability status of the room (e.g., vacant, occupied, under maintenance).	tinyint
	1		
patient_patientID	Represents the unique identifier of the patient currently occupying the room, if any.	int
	2-3		PK
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/c55bbe60-8253-4dd6-b79e-9c0d780be812)


Table: Rooms_has_Equiqment
Col. Name	Description	Data Type	Size	Format	Key?

Rooms_roomNum
 	Represents the room number associated with a specific room.	int	1		PK

Rooms_patient_patientID	Represents the unique identifier of the patient assigned to a particular room.	int
	3		PK
Equiqment_Equiqment_ID	Represents the unique identifier for an equipment item.	int	4		PK
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/7c27ac73-ea70-4c1e-ada3-d6f291a825cb)


Table: Staff
Col. Name	Description	Data Type	Size	Format	Key?

staffID	Represents the unique identifier for a staff member.	int 
	4		PK
staffName
	Represents the name of a staff member.	varchar(45)
	45		
staff_Role
	Represents the role or position of a staff member within the organization.	varchar(45)
	45		
staff_schedule	Represents the role or position of a staff member within the organization.	varchar(45)
	45		
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/68567f51-49c5-4419-a97c-4978bfcfaecc)

Table: Transportation
Col. Name	Description	Data Type	Size	Format	Key?

Name
 	Represents the name of the type of transportation (ambulance, ER, helicopter)	varchar(45)
	45		PK
DESC
	Provides an optional brief explanation or definition.	varchar(45)
	45		
License_Plate
	Represents the license plate number of a vehicle.	varchar(45)
	45		
Driver
	Stores the name of the driver associated with a vehicle.	varchar(45)
	45		
patient_patientID	Refers to the unique identifier for a patient.	int	1-3		PK
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/4b008397-dfb8-4a67-8e00-613adff635a2)



SQL Queries: 
4 Simple Queries:

#1 Select the name and DOB for all patients born in 1999

SELECT patient_Name, `date of birth` 
FROM patient
WHERE `date of birth` regexp "1999";
 
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/7d154fba-6b84-41eb-9e33-563152b20adf)

#2 Show the name of patient and show their invoice number and amount due

SELECT patient_Name, Invoice_InvoiceNum, Charge
FROM patient
JOIN patient_has_Invoice ON patient_has_Invoice.patient_patientID = patient.patientID;
 
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/87a7325a-d665-432f-a081-8ce89ba3a43b)

#3 Display all existing appointments along with the date and name of patient

SELECT patient_Name, appointmentID, Date
FROM patient
JOIN Appointment ON Appointment.patient_patientID= patient.patientID;

 ![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/6a13ed8f-2265-483f-851a-6becad0ef241)

 #4 Display all appointments for a particular staff member

SELECT staffID, staffName, staff_schedule,appointmentID, Date
FROM Staff
JOIN Appointment ON Appointment.Staff_staffID = Staff.staffID
WHERE staffID = "1552";
 
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/8a50805f-ba58-4523-8887-3b9d076db28f)

6 Complex Queries:
#1 Display the patient name, DOB, and their review number and review description

SELECT p.`date of birth`,p.patient_Name, r.reviewNum, r.Desc
FROM patient p
JOIN Review r ON p.patientID = r.patient_patientID;
 
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/2a6c7311-c0bb-403c-a920-1206c5824fe5)

#2 Find all appointments scheduled for 2027-10-21 along with the patient's name and the staff assigned to each appointment.

SELECT a.appointmentID, a.Date, p.patient_Name, s.staffName
FROM Appointment a
JOIN patient p ON a.patient_patientID = p.patientID
JOIN Staff s ON a.Staff_staffID = s.staffID
WHERE DATE(a.Date) ='2027-10-21';
 
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/3cc0d5a3-3097-4d41-8844-3a1be3ec0de6)

#3 Evaluate staff performance based on the number of appointments attended and the corresponding average patient reviews.

SELECT s.staffID, s.staffName,  
COUNT(a.appointmentID) AS num_appointments_attended, 
AVG(r.Rating) AS average_review_rating
FROM Staff s
JOIN Appointment a ON s.staffID = a.Staff_staffID
JOIN Procedures pr ON a.appointmentID = pr.Appointment_appointmentID
JOIN patient p ON p.patientID = a.patient_patientID
JOIN Review r ON r.patient_patientID = p.patientID
GROUP BY s.StaffID, s.StaffName;
 
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/9be46af7-9e28-4ea7-97be-fde83292ddbf)


#4 Retrieve all appointments scheduled for Cesaro Troake along with their emergency contact details. 

SELECT a.appointmentID, a.Date, e.EC_Phone, e.EC_Address, p.patient_Name
FROM Appointment a
JOIN patient p ON a.patient_patientID = p.patientID
JOIN Emergency_Contact e ON p.patientID = e.patient_patientID
WHERE p.patient_Name = 'Cesaro Troake’;
 
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/b87a3ad2-5716-4e4c-ac9b-6259e5ce88ad)


#5 Determine the average number of appointments per staff member over a given period, and display those exceeding the average in descending order

SELECT 
    Staff.staffID, 
    Staff.staffName, 
    COUNT(Appointment.appointmentID) AS NumberOfAppointments
FROM Staff
JOIN Appointment ON Staff.staffID = Appointment.Staff_staffID
WHERE Appointment.Date BETWEEN '2025-08-25' AND '2027-11-03'
GROUP BY Staff.staffID, Staff.staffName
HAVING 
    COUNT(Appointment.appointmentID) > (
        SELECT (AVG(AppointmentCounts.NumberOfAppointments) - 0.1) -- Slight adjustment for precision
        FROM (
            SELECT COUNT(Appointment.appointmentID) AS NumberOfAppointments
            FROM Appointment
            WHERE Appointment.Date BETWEEN '2025-08-25' AND '2027-11-03'
            GROUP BY Appointment.Staff_staffID
        ) AS AppointmentCounts
    )
ORDER BY NumberOfAppointments DESC;

 
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/381c3eb0-4119-4cfa-bd71-5da65a3da5d2)
 

#6 Identify patients with the largest balance due on their invoices with a balance exceeding $10,000. Order the balances due in descending order and display the total average balance due.

SELECT 
    patient.patientID,
    patient.patient_Name,
    Invoice.InvoiceNum,
    SUM(Invoice.Balence_Due) AS TotalBalanceDue,
    (SELECT AVG(Balence_Due) FROM Invoice) AS TotalAverageBalanceDue
FROM patient
JOIN patient_has_Invoice ON patient.patientID = patient_has_Invoice.patient_patientID
JOIN Invoice ON patient_has_Invoice.Invoice_InvoiceNum = Invoice.InvoiceNum
GROUP BY patient.patientID, patient.patient_Name, Invoice.InvoiceNum
HAVING SUM(Invoice.Balence_Due) > 10000
ORDER BY TotalBalanceDue DESC;

 
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/64f9be0c-cb14-4f6c-911b-e3355398da8a)

