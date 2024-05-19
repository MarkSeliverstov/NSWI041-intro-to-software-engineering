## Student: selivem

### Use case: [Data editing](https://gitlab.mff.cuni.cz/budaipe/nswi041_pri/-/blob/master/use_cases/all_cases.md?ref_type=heads#data-editing-edit%C3%A1cia-%C3%BAdajov)

#### Test conditions

1. Applicant can access the platform.
2. Applicant can log into the system using valid credentials.
3. Applicant can view a list of available data/documents to edit.
4. Applicant can select specific data/documents to edit.
5. Applicant can make changes to the selected data/documents.
6. Applicant can submit the changes for approval.
7. System processes and submits the changes.
8. System notifies the applicant about the (non-)successful submission.
9. System doesn't save non-valid submission.
10. System successfully saves valid submission.
11. System will rollback the changes if the submission is not successful.
12. Institution has provided the feature to allow data editing by applicants.
13. system supports role-based access control to ensure only authorized
    applicants can edit specific data/documents.

### Test case 1

| ID | TC_1 |
| --- | ---|
| Title | Viewing and selecting available data/documents to edit |
| Priority | High |
| Preconditions | Applicant has account in the system. Applicant is logged in. |
| Post conditios | Applicant can view a list of available data/documents to edit. Applicant can select specific data/documents to edit. |
| Role | Applicant |
| Test data | ... |
| Covered test conditions | 1, 2, 3, 4 |

| Test steps | Action | Expected result | Result | Comment |
| --- | ---| --- | --- | ---|
| 1 | Applicant logs into the system with right credentials | Opening menu of the system is shown to the applicant | OK | ... |
| 2 | Applicant selects "Edit data" from the menu | List of available data/documents to edit is shown | OK | ... |
| 3 | Applicant selects specific data/document to edit | Data/document is selected | OK | ... |

### Test case 2

| ID | TC_2 |
| --- | ---|
| Title | Error handling and rollback |
| Priority | High |
| Preconditions | Applicant has account in the system. Applicant is logged in. |
| Post conditios | System will rollback the changes if the submission is not successful. |
| Role | Applicant |
| Test data | ... |
| Covered test conditions | 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11 |

| Test steps | Action | Expected result | Result | Comment |
| --- | ---| --- | --- | ---|
| 1 | Applicant logs into the system with right credentials | Opening menu of the system is shown to the applicant | OK | ... |
| 2 | Applicant selects "Edit data" from the menu | List of available data/documents to edit is shown | OK | ... |
| 3 | Applicant selects specific data/document to edit | Data/document is selected | OK | ... |
| 4 | Applicant makes changes to the data/document | Changes are made | OK | ... |
| 5 | Applicant submits the changes | System processes the changes | Error | ... |
| 6 | System notifies the applicant about the error | Applicant is notified | OK | ... |
| 7 | System rolls back the changes | Data/document is reverted to the previous state | OK | ... |
