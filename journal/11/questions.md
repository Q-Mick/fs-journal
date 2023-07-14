# A bit more CSharp and SQL
1. What does ***inheritance*** accomplish for us in C#?

  > | allows classes to inherit properties or methods.  |

2. How does ***member inheritance*** work in C#? Does a `Class` inherit all members of the base `Class`?

  > | The class inherits the members of another class aka derived class and the class members inherited are the base class. Inheritance in C# enables you to create new classes that reuse, extend, and modify the behavior defined in other classes.|

3. How does ***accessibility*** affect inheritance?

  > | The access specifiers only affect whether outsiders and derived classes can access those members. Second, when derived classes inherit members, those members may change access specifiers in the derived class. |

4. What is the difference between a `PRIMARY KEY` and a `FOREIGN KEY`

  > | A primary key uniquely identifies a row in a table, while a foreign key is used to link two tables together by referencing the primary key of the related table. |

5. What is an ***alias***?

  > |  Aliasing refers to a scenario when two or more variables refer to the same value in memory. basically you call Reports rep for short so you can say rep.id instead of reports.id |

6. Demonstrate how you would query a join statement that would get all of a doctors patients from the following collections:

  ```SQL
  CREATE TABLE doctors (
    id INT NOT NULL AUTO_INCREMENT,
    -- CODE OMITTED
    PRIMARY KEY (id)
  )

  CREATE TABLE patients (
    id INT NOT NULL AUTO_INCREMENT,
    -- CODE OMITTED
    PRIMARY KEY (id)
  )

  CREATE TABLE patient_doctors (
    id INT NOT NULL AUTO_INCREMENT,
    doctorId INT NOT NULL,
    patientId INT NOT NULL,

    FOREIGN KEY (doctorId)
      REFERENCES doctors(id),
    FOREIGN KEY (patientId)
      REFERENCES patients(id),
  )

  ```

  > | SELECT * FROM doctors JOIN patients ON doctors.id = patients_doctor.id |
