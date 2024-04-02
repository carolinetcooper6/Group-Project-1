# Group-Project-1
Group 1: 
Group Members: 
Caroline 
Gwen
Charlie
Hubah 
Kishen

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
Table: APPOINTMENT
Col. Name	Description	Data Type	Size	Format	Key?
appointmentID	Unique sequential number indicating the identification number of the appointment	int	5		PK
Date	Date of the specific appointment	Date	10		
Appointmentcol*	Optional additional appointment notes	Varchar(45)			
patient_patientID	Unique sequential number indicating the identification number of the corresponding patient with the appointment	int	3		PK
Staff_staffID	Unique sequential number indicating the identification number of the corresponding staff member for the appointment	int	4		PK

 Table: EMERGENCY_CONTACT
Col. Name	Description	Data Type	Size	Format	Key?
EC_ID	Unique sequential number indicating the identification number of the specific instance of an emergency contact	int	2-4		PK
EC_Phone	Phone number of each emergency contact	Varchar(45)	12		
EC_Address	Address of each emergency contact	Varchar(45)	45		
EC_Other	Additional Info (optional)	Varchar(45)	45		
patient_patientID	Unique sequential number indicating the identification number of the corresponding patient 	int	3		PK





Table: EQUIPMENT (Note: should have been EQUIPMENT—TYPO)
Col. Name	Description	Data Type	Size	Format	Key?
Equipment_ID	Unique sequential number indicating the identification number of equipment	int	4		PK
Type	Name of the type of equipment	Varchar(45)	45		
Description	Optional text description of equipment	Varchar(45)	45		
Quantity	Quantity of type of equiptment	int	1-2		
Expiration_Date	Expiration date of equiptment	Date	10		

Table: INVOICE
Col. Name	Description	Data Type	Size	Format	Key?
InvoiceNum	Unique sequential number indicating the identification number of each invoice	Int	4-6		PK
days_of_Stay	Number of days of stay	Int	2-3		
Balence_Due	Monetary balance due	Int	4-5		
Note: TYPO (meant Balance_Due)
![image](https://github.com/carolinetcooper6/Group-Project-1/assets/165078010/efbcf7b2-112c-4103-b093-bd4d48de85e8)


