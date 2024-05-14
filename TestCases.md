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
6. Prompt to provide necessary documents.
7. Prompt to provide necessary information (fill info on the web).
8. Validation of documents "properties" (max. size, format) (Ask ?? je potreba specifikovat jaka kriteria, nebo psat obecne, je to az moc dopodrobna?)
9. Validation of information filled on web.
10. Saving uploaded documents.
11. Saving information filled on web.
12. Continue without prompt to provide additional data.
13. Applicant submitted request to the system.
14. System processed request.
15. System saves valid submission.
16. System notifies applicant about successful submission.
17. System doesnt save non-valid submission.
18. System notifies applicant about non-successful submission request.
19. Service "application for waiver of entrance exams" is unavaliable due to expiration date.
20. Service "application for waiver of entrance exams" is unavaliable because program doesnt have entrance exam.
21. Service "application for waiver of entrance exams" is unavaliable because entrance exam is mandatory for everyone.
22. Service "application for waiver of entrance exams" is unavaliable due to change in admission process.
23. Service notifies applicant about unavailability of the service "" due to change in admission process.
24. System reflects changes in admission process (when waiver of entrance exams is no longer possible).
25. System doesnt provide opportunity to submit more than one valid "Application for waiver of entrance exams" for 1 program from 1 applicant in 1 admission process.

### Test case 1
| ID | TC_1 |
| --- | ---|
| Title | Submission of application for waiver of entrance exams |
| Priority | Medium |
| Preconditions | ... |
| Post conditios | ... |
| Role | Applicant |
| Test data | ... |
| Covered test conditions | ... |

| Test steps | | | | |
| --- | ---| --- | --- | ---|
| # | Action | Expected result | Result | Comment |
| 1 | Applicant logs into the system with right credentials | Opening menu of the system is shown to the applicant | OK | nothing |



