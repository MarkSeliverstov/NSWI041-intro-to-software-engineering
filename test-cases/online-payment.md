## Student: Popova
### Use case: Payment of application fee - online
#### Test conditions.
1. The system notifies the applicant of not yet paid application
2. The system monitors deadline for each application
3. After the deadline there is no option to pay for an application
4. The applicant sees the applications he has applied for
5. The system correctly notes paid and unpaid applications
6. Available payment options are displayed
7. Payment detailes are displayed
8. The system redirects to the external payment processor
9. After the successful payment, the applicant is redirected back to the applicant's account
10. The system notifies the applicant about a successful payment
11. The system notifies the applicant about a failure in payment
12. If applicant does not finish the payment, payment data is invalidated and deleted
13. If applicant fills in invalid payment details, payment data is invalidated and deleted
14. If applicant cancels the payment, payment data is invalidated and deleted
15. The money received for an invalid payment is returned immediately
16. The money received for a valid payment is charged to university's bank account
17. After receiving the payment the state "paid" of the application is stored

### Test case 1
| ID | TC_1 |
| --- | --- |
| Title | Online payment of application fee |
| Priority | High |
| Preconditions | The applicant has an account with an at least one unpaid application and is logged in to the system |
| Post conditios | The application is paid |
| Role | Applicant |
| Test data | --- |
| Covered test conditions | 4, 5, 6, 7, 8, 9, 10, 15, 16 |

| Test steps | | | | |
| --- | ---| --- | --- | ---|
| # | Action | Expected result | Result | Comment |
| 1 | Applicant logs in to the system with the right credentials | Applicant profile is displayed | OK | ... |
| 2 | Applicant selects the unpaid application | The details of the application are displayed | OK | ... |
| 3 | Applicant clicks "Pay online" | Payment methods are displayed | OK | ... |
| 4 | Applicant selects a payment method | Relevant fields are displayed | OK | ... |
| 5 | Applicant fills in payment info | The system checks the format correctness | OK | ... |
| 6 | Applicant clicks "Pay" | The system redirects to the external payment processor where the payment is being processed | OK | ... |
| 7 | The message about successful payment is displayed, applicant is redirected back to the student system | Money was sent and charged to the university bank account | OK | ... |
| 8 | Applicant selects the same application | The application is in paid state | OK | ... |


### Test case 2
| ID | TC_2 |
| --- | --- |
| Title | Invalid online payment of application fee |
| Priority | High |
| Preconditions | The applicant has an account with an at least one unpaid application and is logged in to the system |
| Post conditios | The application is unpaid, no money was charged |
| Role | Applicant |
| Test data | --- |
| Covered test conditions | 4, 5, 6, 7, 8, 11, 13 |

| Test steps | | | | |
| --- | ---| --- | --- | ---|
| # | Action | Expected result | Result | Comment |
| 1 | Applicant logs in to the system with the right credentials | Applicant profile is displayed | OK | ... |
| 2 | Applicant selects the unpaid application | The details of the application are displayed | OK | ... |
| 3 | Applicant clicks "Pay online" | Payment methods are displayed | OK | ... |
| 4 | Applicant selects a payment method | Relevant fields are displayed | OK | ... |
| 5 | Applicant fills in invalid payment info | The system checks the format correctness | OK | ... |
| 6 | Applicant clicks "Pay" | The system redirects to the external payment processor where the payment is being processed | OK | ... |
| 7 | The error message is displayed, applicant closes the tab | No money was sent or charged, payment data is invalidated and deleted | OK | ... |
| 8 | Applicant selects the same application | The application is in unpaid state | OK | ... |
