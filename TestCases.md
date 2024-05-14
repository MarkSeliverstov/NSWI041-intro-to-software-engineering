# Test cases
Task: 1 use case per team member, 2 test cases from each memeber for their 1 use case.

## Student: Korop
### Use case: [Application for waiver of entrance exams (Žiadosť o odpustenie prijímacích skúšok)](https://gitlab.mff.cuni.cz/budaipe/nswi041_pri/-/blob/master/use_cases/all_cases.md?ref_type=heads#application-for-waiver-of-entrance-exams-%C5%BEiados%C5%A5-o-odpustenie-prij%C3%ADmac%C3%ADch-sk%C3%BA%C5%A1ok)
#### Test conditions.
1. Applicant submitted valid application form.
2. Program (the applicant applied for) has option for waiver.
3. Option for waiver expiration (whether expired or not at different period of time). (?? Ask, co zde jde testovat expiraci nebo validost nebo oboje)
4. Applicant logged into the system.
5. Admission process selection.
6. Applicant chooses to submit "application for waiver of entrance exams".
7. Prompt to provide necessary documents.
8. Prompt to provide necessary information (fill info on the web).
9. Validation of documents "properties" (max. size, format) (Ask ?? je potreba specifikovat jaka kriteria, nebo psat obecne, je to az moc dopodrobna?)
10. Validation of information filled on web.
11. Saving uploaded documents.
12. Saving information filled on web.
13. Continue without prompt to provide additional data.
14. Applicant submitted request to the system.
15. System processed request.
16. System saves valid submission.
17. System notifies applicant about successful submission.
18. System doesnt save non-valid submission.
19. System notifies applicant about non-successful submission request.
20. Service "application for waiver of entrance exams" is unavaliable due to expiration date.
21. Service "application for waiver of entrance exams" is unavaliable because program doesnt have entrance exam.
22. Service "application for waiver of entrance exams" is unavaliable because entrance exam is mandatory for everyone.
23. Service "application for waiver of entrance exams" is unavaliable due to change in admission process.
24. Service notifies applicant about unavailability of the service "" due to change in admission process.
25. System reflects changes in admission process (when waiver of entrance exams is no longer possible).
26. System doesnt provide opportunity to submit more than one valid "Application for waiver of entrance exams" for 1 program from 1 applicant in 1 admission process.
27. Applicant sees status, information about their application for study program.

### Test case 1
| ID | TC_1 |
| --- | ---|
| Title | Submission of application for waiver of entrance exams |
| Priority | Medium |
| Preconditions | Applicant has account in the system. Applicant submitted valid application for some valid program with entrance exam,  |
| Post conditios | Applicant successfully submitted "application for waiver of entrance exams". "Application for waiver of entrance exams" for the applicant is saved in the system, Applicant cannot submit another "application for waiver of entrance exams" for that program during that admission process |
| Role | Applicant |
| Test data | ... |
| Covered test conditions | 1, 2, 4, 5, 6, 7, 9, 11, 14, 15, 16, 17, 27 |

| Test steps | | | | |
| --- | ---| --- | --- | ---|
| # | Action | Expected result | Result | Comment |
| 1 | Applicant logs into the system with right credentials | Opening menu of the system is shown to the applicant | OK | nothing |
| 2 | Applicant selects relevant admission process | Information, status and options of the process are shown | OK | ... |
| 3 | Applicant chooses to submit "application for waiver of entrance exams" | New window with fields where to upload documents is shown | OK | ... |
| 4 | Applicant uploads documents | After validation of max. size, format window reflects that files were uploaded | OK | ...|
| 5 | Applicant confirms the submission of the application | System saves the application, System notifies applicant about successful submission | OK | ... |
### Test case 2
| ID | TC_2 |
| --- | ---|
| Title | Submission of application for waiver of entrance exams, when already submitted successfully |
| Priority | Medium |
| Preconditions | Applicant has account in the system. Applicant submitted valid application for some valid program with entrance exam, Applicant has already submitted valid "Application for waiver of entrance exams". System saved valid application. |
| Post conditios | State in the system did not change. First valid application is saved in the system. Second application is not in the system. |
| Role | Applicant |
| Test data | ... |
| Covered test conditions | 1, 2, 3, 4, 5, 6, 26 |

| Test steps | | | | |
| --- | ---| --- | --- | ---|
| # | Action | Expected result | Result | Comment |
| 1 | Applicant logs into the system with right credentials | Opening menu of the system is shown to the applicant | OK | nothing |
| 2 | Applicant selects relevant admission process | Information, status and options of the process are shown | OK | ... |
| 3 | Applicant selects option to submit "application for waiver of entrance exams" | (System checks for already submitted applications,) and returns notification that the applicant cannot submit the "application for waiver of entrance exams", as there is already submitted application in the system | OK | ... |



