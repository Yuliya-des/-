# - Диаграмма классов
![diagram](http://www.plantuml.com/plantuml/png/fLD1ReGm3Bpd5JvknUO7AxGLfqghgb9VG26baI18iNDgz--rYCE6L8X3JzZZP3mUXojIwobCesh65X7UZCVPmRVIO1s1cwSFupb1yjODuDh9S7QpI9Tc3XvD3TtoHL0Ll5FeZQDJTlg9OKa7Gw-Cd1ZQCd0XXhZKkF5oTkaD3DsL4bsN7wrJ5zYYDzDHy2nM9f5JHwEmUZIuqQFkYIDn_eia0aSKQwjHWcIpp543nW1L9PJ7Dl-riYf8kIXnz7wLmOKKomhML7ixV94M5Kebf_LeFbSuJV_Ya2m5ilAgCiqfGsZxtXl41z3DZjgESDU4dKUOuAIrNkraspPQSlFEXOvpAMF7tGVq72yMQ2FNZtm_-1-AYRBDb8lHSpwZKf6bnBED5OMhSNsOnby0)
```Java
@startuml
Class Person {
- int nomber
- string name
- List<Course> courses 
+ Student(string name)
+ string getName()
+ List<Course> getCourses()
+ int getNomber ()
}

Person <|-- Student 

Person <|-- Lecturer

Class Student {
- int nomber
- string name
- couses List<Course>
}

Class Lecturer {
- int nomber
- string name
- couses List<Course>
}

Class Course {
- int nomber
- string name
- Lecturer lecturer
- List<Student> students
+ Course(string name)
+ string getName()
+ int getNomber ()
+ List<Student> getStudents()
+ Lecturer getLecturer ()
}

Lecturer -right- Course

Student -left- Course

Class Institution {
- string name
- strins address
- strins contacts
- List<Student> students
- List<Course> courses
- List<Lecturer> lecturers
+ Institution (string name, strins address, strins contacts)
+ string getName()
+ string getAddress()
+ string getContacts()
+ List<Student> getStudents()
+ List<Course> getCourses()
+ List<Lecturer> getLecturer()
}

Lecturer --o Institution

Course --o Institution

Student --o Institution
@enduml
```
