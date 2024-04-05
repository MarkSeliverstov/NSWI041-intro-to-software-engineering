```
@startuml
package Person {
object Student
object Teacher
object Study_Dep_st
}


object User_Profile
object Person_log

Person --|> User_Profile : Searching for profile
Person --|> User_Profile : Has Profile
Person --|> User_Profile : Editing own Profile
Person --|> Person_log : Has log

Study_Dep_st --|> Person_log : Viewing log
Study_Dep_st --|> User_Profile : Editing smb's Profile

Student -- Student : Sending friend Request
Student -- Student : Accepting friend Request
@enduml
```
![XP71JiGW48RlynHpyxGluC6iYIOU6rUz4fREjcWBE4pJ6FNTHKBJcf1wOuPlVdx-EKRHBDCuGD3cJNU43N7q3Z_1dr_929vaQid9KZwHDZtnzlP3tL5GKU0ROEa_HsBLiB_OWKglAAl1Tm3bbSFXw-OFYzTu8iscjwx3YsSCHMDdu457RFx7xbihlwf-TbLyjLSqiz7j1olSYwKvYMPsY-uwYEFvQhKC9U4qieITKt1jpe1jEk4ZlKyKfS](https://github.com/MarkSeliverstov/NSWI041-intro-to-software-engineering/assets/120932204/0f44415f-4d12-4d6e-b6d4-194d5ea8d454)
