### Use case: [Creating a new application](https://gitlab.mff.cuni.cz/budaipe/nswi041_pri/-/blob/master/use_cases/all_cases.md?ref_type=heads#creating-a-new-application)

#### Test conditions

1. Applicant can log into the system successfully.
2. System displays the option to create a new application.
3. Applicant can fill in all required details for the new application.
4. System validates the entered details.
5. Applicant submits the application.
6. System stores the application data correctly.
7. System sends a notification about successful application creation.
8. Applicant can cancel the application creation process.
9. System handles errors for invalid data input.
10. System handles application attempts after the deadline.
11. System checks for duplicate applications.
12. System prevents submission if the application is incomplete.
    
### Test case 1

| ID | Test case 1 |
| --- | --- |
| Title | Creating a New Application Successfully |
| Priority | High |
| Preconditions | The applicant has an account in the system and is logged in. The faculty has opened the application process for applicants. |
| Postconditions | The applicant is notified about the successful creation of the application. The valid application is stored in the system database. |
| Role | Applicant |
| Test data | ... |
| Covered tests conditions | 1, 2, 3, 4, 5, 6, 7, 11, 12 |

| Test step | Action | Expected Result | Result |	Comment |
| --- | --- | --- | --- | --- | 
| 1. |  Applicant logs into the system with the correct credentials. | 	Opening menu of the system is shown to the applicant. | 	OK	 |  | 
| 2. |  Applicant selects "Create New Application" from the menu. | 	Form for creating a new application is displayed. | 	OK	 |  | 
| 3. |  Applicant fills in the required details (study programme, language, form of study). | 	Details are correctly filled in and shown in the form. | 	OK	 |  | 
| 4. |  Applicant submits the application.	 | System processes the data and validates the entered details. | 	OK	 |  | 
| 5. |  System confirms the application is valid and processes the data. | 	Confirmation message about successful creation is displayed. | 	OK	 |  |  
| 6. |  System stores the provided data in the internal system. | 	Data is successfully stored in the system database. | 	OK	 |  | 
| 7. |  System sends a notification to the applicant about the successful creation of the application. | 	Applicant receives a notification (e.g., email or system message) confirming the successful creation. | 	OK	 |  | 

### Test case 2

| ID | Test case 2 |
| --- | --- |
| Title | Application Creation Error Due to Past Deadline |
| Priority | Medium |
| Preconditions | The applicant has an account in the system and is logged in. The faculty application deadline has passed. |
| Postconditions | The applicant is notified that the application cannot be created because the deadline has passed. No application data is stored in the system. |
| Role | Applicant |
| Test data | ... |
| Covered tests conditions | 1, 2, 3, 4, 5, 10, 12 |

| Test step | Action | 	Expected Result | 	Result	 | Comment | 
| ---  | --- | --- | --- | --- | 
| 1. |  Applicant logs into the system with the correct credentials. | 	Opening menu of the system is shown to the applicant. | 	OK	  |  | 
| 2. |  Applicant selects "Create New Application" from the menu.	 | Form for creating a new application is displayed.	 | OK	 |  | 
| 3. |  Applicant fills in the required details (study programme, language, form of study). | 	Details are correctly filled in and shown in the form. | 	OK	 |  | 
| 4. |  Applicant submits the application. | 	System processes the data and checks the application deadline.	 | OK	 |  | 
| 5. |  System identifies that the application deadline has passed.	 | Error message is displayed to the applicant stating that the application cannot be created due to past deadline.	 | OK	 |  | 
| 6. |  System does not store any application data.	 | No data is stored in the system database.	 | OK	 |  | 
| 7. |  System sends a notification to the applicant about the inability to create the application. | 	Applicant receives a notification (e.g., email or system message) about the inability to create the application. | 	OK |  | 
