# Day-05-Practicals Session


## Description
A Spring Boot application for managing students, courses, and instructors with basic CRUD operations.


## API Endpoints

### Student Controller (`/students`)
- `GET /students` - Get all students
- `GET /students/{regNo}` - Get student by registration number
- `POST /students` - Create new student
- `PUT /students/{regNo}` - Update student
- `DELETE /students/{regNo}` - Delete student

### Course Controller (`/course`)
- `GET /course` - Get all courses
- `GET /course/{code}` - Get course by code
- `POST /course` - Create new course
- `PUT /course/{code}` - Update course
- `DELETE /course/{code}` - Delete course

### Instructor Controller (`/instructor`)
- `GET /instructor` - Get all instructors
- `GET /instructor/{empID}` - Get instructor by employee ID
- `POST /instructor` - Create new instructor
- `PUT /instructor/{empID}` - Update instructor
- `DELETE /instructor/{empID}` - Delete instructor

## Models

### Student
- `name`: String
- `age`: int
- `regNo`: String (unique identifier)
- `course`: String
- `gpa`: double

### Course
- `name`: String
- `code`: String (unique identifier)
- `credits`: int
- `lecturer`: String

### Instructor
- `name`: String
- `empID`: int (unique identifier)
- `subject`: String

## Sample Data

### Students
| Registration No | Name            | Age | Course | GPA |
|-----------------|-----------------|-----|--------|-----|
| IT1023          | Rashmika        | 24  | DS     | 3.2 |
| IT1038          | Maduranga       | 25  | SE     | 3.3 |
| IT1068          | Sanchitha       | 23  | ML     | 3.4 |

### Courses
| Code   | Name         | Credits | Lecturer     |
|--------|--------------|---------|--------------|
| IT3232 | ECommerce    | 2       | A.john       |
| IT2234 | WebServices  | 3       | J.devide     |
| IT3132 | SQA          | 1       | J.rebe       |

### Instructors
| Employee ID | Name        | Subject     |
|-------------|-------------|-------------|
| 15012       | carni       | ECommerce   |
| 15065       | mari        | WebServices |
| 15098       | alen        | SQA         |

## Technology Stack
- Java 17
- Spring Boot 3.x
- RESTful Web Services
- Maven (assumed)

## Installation & Usage

1. Clone the repository
2. Import as Maven project in your IDE
3. Run the Spring Boot application
4. Access endpoints using:
   - http://localhost:8080/students
   - http://localhost:8080/course
   - http://localhost:8080/instructor



- Built using a generic CRUDController superclass for common operations
- In-memory data storage using HashMap
- All controllers implement standard CRUD operations
