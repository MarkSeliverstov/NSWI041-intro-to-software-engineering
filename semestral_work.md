# Student information system - Person module

[*Module description*]

## Functional Requirements

This section specifies the functional requirements.

### User requirements

[*List of user requirements in a form of user stories*]

### System requirements

#### Actors

- Teacher: Person, that teaches courses, supervise thesis, ... 
- Student: Person, that studies at university
- Study Department staff: Person, that works at Study Departmant. Manages administartive smth ...

#### Use cases
##### 1. Use cases for user stories 1, 2, 3, 4, 6, 8 (prototype)

[*Use case diagram in PlantUML*]

```plantuml
@startuml
scale 2
left to right direction
skinparam PackageStyle rect
actor Student
actor Teacher
actor "Study Department Worker" as sd
rectangle PersonModule {
    ' 2 user story
    Student -- (View their own Personal Info)
    Teacher -- (View their own Personal Info)
    ' 1 user story
    (View their own Personal Info) --> (Edit Personal Info): extend
    (Edit Personal Info) --> (Save To User Activity Log): include
    (Set up visibility) --> (Save To User Activity Log): include
    (Edit Personal Info) --> (Confirm changes): include
    (Set up visibility) --> (Confirm changes): include
    ' (Save Changes) ??
    ' 3 user story
    (View their own Personal Info) --> (Set up visibility): extend
    ' 4 user story
    Student -- (Search for Person)
    Teacher -- (Search for Person)
    ' 6 user story, for student and teacher different permissions for visibility are set
    (Search for Person) --> (View smb's Personal Info) : extend

    ' 8 user story
    sd -- (Check User Activity logs)
    (Check User Activity logs) --> (Confirm changes): extend
    (Check User Activity logs) --> (Alert??) : extend
    sd -- (Edit other Person Info)
    (Edit other Person Info) --> (Confirm changes): include
}
@enduml
```

[*Describe the diagram in a short paragraph. Describe each use case from the diagram in the detail from the lecture in a separate subsection.*]

###### [*Use case title*]

[*Use case description in the structure from the lecture.*]

[*Add an activity diagram for one use case per a team member*]

## Information model

[*Express the information model of the domain as a UML class diagram in PlantUML. Do not use class methods in the diagram, only classes, class attributes and associations connecting classes.*]

```plantuml
@startuml
class Car

Driver - Car : drives >
Car *- Wheel : have 4 >
Car -- Person : < owns
@enduml
```

[*Document each class with in a separate subsection*]

### [*Class name*]

[*Class description consisting of its definition, description of its essential properties (attribues and associations).*]
