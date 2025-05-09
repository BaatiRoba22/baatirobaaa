# baatirobaaa


Students Table

| Column Name    | Data Type      | Constraints                      |
| :------------- | :------------- | :------------------------------- |
| student_id     | INT            | PRIMARY KEY, AUTO_INCREMENT      |
| first_name     | VARCHAR(255)   | NOT NULL                         |
| last_name      | VARCHAR(255)   | NOT NULL                         |
| date_of_birth  | DATE           |                                  |
| email          | VARCHAR(255)   | UNIQUE                           |
| phone_number   | VARCHAR(20)    |                                  |
| address        | VARCHAR(255)   |                                  |

Courses Table

| Column Name     | Data Type      | Constraints                      |
| :-------------- | :------------- | :------------------------------- |
| course_id       | INT            | PRIMARY KEY, AUTO_INCREMENT      |
| course_name     | VARCHAR(255)   | NOT NULL                         |
| course_description | TEXT           |                                  |
| credits         | INT            |                                  |

Enrollments Table

| Column Name      | Data Type      | Constraints                      |
| :--------------- | :------------- | :------------------------------- |
| enrollment_id    | INT            | PRIMARY KEY, AUTO_INCREMENT      |
| student_id       | INT            | FOREIGN KEY referencing Students |
| course_id        | INT            | FOREIGN KEY referencing Courses  |
| enrollment_date  | DATE           |                                  |

Grades Table

| Column Name     | Data Type      | Constraints                      |
| :-------------- | :------------- | :------------------------------- |
| grade_id        | INT            | PRIMARY KEY, AUTO_INCREMENT      |
| enrollment_id   | INT            | FOREIGN KEY referencing Enrollments |
| grade           | VARCHAR(2)     |                                  |
| grade_date      | DATE           |                                  |

