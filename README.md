# 🏥 Smart Clinic Management System - Java Full-Stack Capstone

<p float="left">
    <img src="https://images.credly.com/size/680x680/images/3e3454d5-8832-41dd-b67f-3089617e9bf1/IBM_20Java_20Developer_20Professional_20Certificate.png" width="300" />
    <img src="https://github.com/Willie-Conway/Java-Database-Capstone-Project/blob/5aa7853ad353fa96659a176b7c2d4bea6742bea3/Screenshots/Healthcare%20system.jpg" width="300" />
</p>

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

## 🚀 Project Status & CI/CD Pipeline

![✅ Compile Java Backend](https://github.com/Willie-Conway/java-database-capstone/actions/workflows/compile-backend.yml/badge.svg)
![🧹 Lint Java Backend](https://github.com/Willie-Conway/java-database-capstone/actions/workflows/lint-backend.yml/badge.svg)
![🐳 Lint Dockerfile](https://github.com/Willie-Conway/java-database-capstone/actions/workflows/lint-docker.yml/badge.svg)
![🌐 Lint Frontend](https://github.com/Willie-Conway/java-database-capstone/actions/workflows/lint-frontend.yml/badge.svg)
<br>
![📊 Code Coverage](https://img.shields.io/badge/Code_Coverage-85%25-brightgreen?style=for-the-badge)
![🚀 Deployment](https://img.shields.io/badge/Deployment-Success-10B981?style=for-the-badge)

## 📖 Project Overview
<p float="left">
    <img src="https://github.com/Willie-Conway/java-database-capstone/blob/main/Screenshots/architecture-diagram.png" width="200" />
    <img src="https://github.com/Willie-Conway/Java-Database-Capstone-Project/blob/80807592dc5aee9b5f21655a5a0ceac6f5f37afb/Screenshots/Adding%20Doctor.png" width="200" />
    <img src="https://github.com/Willie-Conway/Java-Database-Capstone-Project/blob/80807592dc5aee9b5f21655a5a0ceac6f5f37afb/Screenshots/Daily%20Appointment%20Report%20by%20Doctor.png" width="200" />
    <img src="https://github.com/Willie-Conway/Java-Database-Capstone-Project/blob/80807592dc5aee9b5f21655a5a0ceac6f5f37afb/Screenshots/Searching%20Doctor.png" width="200" />
    <img src="https://github.com/Willie-Conway/Java-Database-Capstone-Project/blob/012e563df79072c75d21053a80d5cc7d8dd3ed62/Screenshots/Appointments%20List.png" width="200" />
    <img src="https://github.com/Willie-Conway/Java-Database-Capstone-Project/blob/80807592dc5aee9b5f21655a5a0ceac6f5f37afb/Screenshots/Doctor%20Portal.png" width="200" />
</p>

**Smart Clinic Management System** is a comprehensive full-stack healthcare application designed to modernize clinic operations. Built as the **Capstone Project for Java Development**, this system integrates multiple technologies to provide a seamless experience for administrators, doctors, and patients.

## 🏥 Live Application Demo

[![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-F97316?style=for-the-badge&logo=docker&logoColor=white)](https://github.com/Willie-Conway/java-database-capstone/deployments) 
[![API Documentation](https://img.shields.io/badge/📚_API_Docs-8B5CF6?style=for-the-badge&logo=swagger&logoColor=white)](http://localhost:8080/swagger-ui.html)
![Production Ready](https://img.shields.io/badge/Production_Ready-10B981?style=for-the-badge&logo=springboot&logoColor=white)

## 🏗️ System Architecture

```
📂 Smart-Clinic-Management-System/
│
├── 📂 backend/                           # Spring Boot Application
│   ├── 📂 src/main/java/com/project/
│   │   ├── 📂 config/                   # Configuration classes
│   │   │   ├── WebConfig.java          # CORS & MVC configuration
│   │   │   ├── SecurityConfig.java     # JWT security setup
│   │   │   └── DatabaseConfig.java     # Multi-DB configuration
│   │   │
│   │   ├── 📂 controllers/             # REST API Controllers
│   │   │   ├── AdminController.java    # Admin endpoints
│   │   │   ├── DoctorController.java   # Doctor management
│   │   │   ├── PatientController.java  # Patient operations
│   │   │   ├── AppointmentController.java # Appointment handling
│   │   │   └── PrescriptionController.java # Prescription CRUD
│   │   │
│   │   ├── 📂 models/                  # JPA & Document entities
│   │   │   ├── Admin.java              # Admin entity (MySQL)
│   │   │   ├── Doctor.java             # Doctor entity (MySQL)
│   │   │   ├── Patient.java            # Patient entity (MySQL)
│   │   │   ├── Appointment.java        # Appointment entity (MySQL)
│   │   │   └── Prescription.java       # Prescription document (MongoDB)
│   │   │
│   │   ├── 📂 DTO/                     # Data Transfer Objects
│   │   │   ├── AppointmentDTO.java     # Appointment DTO
│   │   │   ├── LoginRequest.java       # Login DTO
│   │   │   └── PrescriptionDTO.java    # Prescription DTO
│   │   │
│   │   ├── 📂 services/                # Business logic layer
│   │   │   ├── AppointmentService.java # Appointment business logic
│   │   │   ├── DoctorService.java      # Doctor operations
│   │   │   ├── PatientService.java     # Patient management
│   │   │   ├── PrescriptionService.java # Prescription handling
│   │   │   └── TokenService.java       # JWT token management
│   │   │
│   │   ├── 📂 repositories/            # Data access layer
│   │   │   ├── AdminRepository.java    # Admin CRUD operations
│   │   │   ├── DoctorRepository.java   # Doctor data access
│   │   │   ├── PatientRepository.java  # Patient repository
│   │   │   ├── AppointmentRepository.java # Appointment repository
│   │   │   └── PrescriptionRepository.java # MongoDB repository
│   │   │
│   │   ├── 📂 mvc/                     # Thymeleaf controllers
│   │   │   ├── DashboardController.java # Dashboard rendering
│   │   │   └── TokenValidationService.java # Session validation
│   │   │
│   │   ├── 📂 utils/                   # Utility classes
│   │   │   ├── Validators.java         # Input validation
│   │   │   ├── DateUtils.java          # Date operations
│   │   │   └── ReportGenerator.java    # Report utilities
│   │   │
│   │   └── BackEndApplication.java     # Main application class
│   │
│   ├── 📂 src/main/resources/
│   │   ├── 📂 static/                  # Frontend assets
│   │   │   ├── 📂 css/                 # Stylesheets
│   │   │   │   ├── adminDashboard.css  # Admin styles
│   │   │   │   ├── doctorDashboard.css # Doctor styles
│   │   │   │   ├── patientDashboard.css # Patient styles
│   │   │   │   └── style.css          # Global styles
│   │   │   │
│   │   │   ├── 📂 js/                  # JavaScript modules
│   │   │   │   ├── 📂 components/      # Reusable components
│   │   │   │   │   ├── appointmentRow.js # Appointment UI
│   │   │   │   │   ├── doctorCard.js   # Doctor card component
│   │   │   │   │   └── patientRecordRow.js # Patient row
│   │   │   │   │
│   │   │   │   ├── 📂 services/        # API services
│   │   │   │   │   ├── appointmentRecord.js # Appointment API
│   │   │   │   │   ├── doctorDashboard.js # Doctor services
│   │   │   │   │   └── patientDashboard.js # Patient services
│   │   │   │   │
│   │   │   │   └── 📂 config/          # Configuration
│   │   │   │       └── apiConfig.js    # API endpoints
│   │   │   │
│   │   │   └── 📂 images/              # Image assets
│   │   │       ├── 📂 logo/            # Brand logos
│   │   │       └── 📂 icons/           # UI icons
│   │   │
│   │   ├── 📂 templates/               # Thymeleaf templates
│   │   │   ├── 📂 admin/               # Admin views
│   │   │   │   └── adminDashboard.html # Admin dashboard
│   │   │   ├── 📂 doctor/              # Doctor views
│   │   │   │   └── doctorDashboard.html # Doctor dashboard
│   │   │   ├── 📂 patient/             # Patient views
│   │   │   │   └── patientDashboard.html # Patient dashboard
│   │   │   └── index.html              # Landing page
│   │   │
│   │   └── application.properties      # Application configuration
│   │
│   ├── 📂 src/test/java/               # Unit & integration tests
│   ├── Dockerfile                      # Backend container definition
│   └── pom.xml                         # Maven dependencies
│
├── 📂 SQL/                            # Database scripts
│   ├── 📂 Stored Procedures/          # MySQL stored procedures
│   │   ├── GetDailyAppointmentReportByDoctor.sql
│   │   ├── GetDoctorWithMostPatientsByMonth.sql
│   │   └── GetDoctorWithMostPatientsByYear.sql
│   │
│   ├── 📂 Seed Data/                  # Initial data
│   │   ├── Insert_into_admin_table.sql
│   │   ├── Insert_into_doctor_table.sql
│   │   ├── Insert_into_patient_table.sql
│   │   ├── Insert_into_appointment_table.sql
│   │   └── Insert_into_doctor_available_times_table.sql
│   │
│   └── cms.sql                        # Complete database schema
│
├── 📂 prescriptions/                  # MongoDB data
│   ├── prescriptions.json             # Sample prescription data
│   └── mongodb-init.js                # MongoDB initialization script
│
├── 📂 .github/workflows/              # CI/CD pipelines
│   ├── compile-backend.yml           # Backend compilation
│   ├── lint-backend.yml              # Java code linting
│   ├── lint-docker.yml               # Dockerfile validation
│   ├── lint-frontend.yml             # Frontend code quality
│   ├── test-backend.yml              # Automated testing
│   └── deploy-production.yml         # Production deployment
│
├── docker-compose.yml                # Multi-container orchestration
├── schema-architecture.md           # System architecture documentation
├── schema-design.md                 # Database design documentation
└── README.md                        # This file
```

## 🎯 Core Features

### **👥 User Role Management**
- **Admin Portal**: Complete system oversight, user management, analytics
- **Doctor Portal**: Appointment management, patient records, prescriptions
- **Patient Portal**: Appointment booking, medical history, prescriptions

### **📅 Appointment System**
- **Real-time Scheduling**: Dynamic appointment booking with availability checking
- **Automated Reminders**: Email/SMS notifications for upcoming appointments
- **Rescheduling & Cancellation**: Flexible appointment management
- **Waitlist Management**: Automatic waitlist handling for fully booked slots

### **💊 Prescription Management**
- **Digital Prescriptions**: Secure electronic prescription generation
- **Medication History**: Complete patient medication tracking
- **Drug Interaction Alerts**: Safety checks for medication combinations
- **Refill Management**: Prescription renewal and refill tracking

### **📊 Analytics & Reporting**
- **Daily Reports**: Appointment summaries by doctor
- **Monthly Analytics**: Patient volume trends
- **Performance Metrics**: Doctor efficiency and patient satisfaction
- **Financial Reports**: Billing and revenue analytics

## 🛠️ Technology Stack

### **Backend**
![Spring Boot 3.2](https://img.shields.io/badge/Spring_Boot_3.2-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![Spring Data JPA](https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=flat-square&logo=spring&logoColor=white)
![JWT Authentication](https://img.shields.io/badge/JWT_Authentication-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)
![REST API](https://img.shields.io/badge/REST_API-FF6C37?style=flat-square&logo=rest&logoColor=white)

### **Databases**
![MySQL 8.0](https://img.shields.io/badge/MySQL_8.0-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MongoDB 7.0](https://img.shields.io/badge/MongoDB_7.0-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Hibernate ORM](https://img.shields.io/badge/Hibernate_ORM-59666C?style=flat-square&logo=hibernate&logoColor=white)

### **Frontend**
![Thymeleaf](https://img.shields.io/badge/Thymeleaf-005F0F?style=flat-square&logo=thymeleaf&logoColor=white)
![Bootstrap 5](https://img.shields.io/badge/Bootstrap_5-7952B3?style=flat-square&logo=bootstrap&logoColor=white)
![Vanilla JavaScript](https://img.shields.io/badge/JavaScript-ES6-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)

### **DevOps**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Maven](https://img.shields.io/badge/Apache_Maven-C71A36?style=flat-square&logo=apachemaven&logoColor=white)
![SonarQube](https://img.shields.io/badge/SonarQube-4E9BCD?style=flat-square&logo=sonarqube&logoColor=white)

## 🚀 Quick Start Guide

### **Prerequisites**
```bash
# Required Software
- Java 17+                    # JDK for Spring Boot
- Maven 3.8+                 # Build tool
- MySQL 8.0+                 # Relational database
- MongoDB 7.0+               # NoSQL database
- Docker & Docker Compose    # Containerization
- Git 2.40+                  # Version control
```

### **1. Clone & Setup**
```bash
# Clone repository
git clone https://github.com/Willie-Conway/java-database-capstone.git
cd java-database-capstone

# Set up databases
mysql -u root -p < SQL/cms.sql
mongo < prescriptions/mongodb-init.js

# Build project
mvn clean install
```

### **2. Configure Environment**
```properties
# application.properties
spring.datasource.url=jdbc:mysql://localhost:3306/cms
spring.datasource.username=root
spring.datasource.password=yourpassword

spring.data.mongodb.uri=mongodb://localhost:27017/prescriptions

jwt.secret=your-512-bit-secret-key-change-in-production
jwt.expiration=86400000
```

### **3. Run Application**
```bash
# Using Maven
mvn spring-boot:run

# Using Docker
docker-compose up --build

# Access application
# Frontend: http://localhost:8080
# API Docs: http://localhost:8080/swagger-ui.html
# Adminer: http://localhost:8081 (Database management)
```

## 📊 Database Architecture

### **MySQL Schema (Relational Data)**
```sql
-- Core Clinic Management Tables
CREATE DATABASE cms;
USE cms;

-- Admin Table
CREATE TABLE admin (
    admin_id INT PRIMARY KEY AUTO_INCREMENT,
    username VARCHAR(50) UNIQUE NOT NULL,
    password_hash VARCHAR(255) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    full_name VARCHAR(100) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Doctor Table
CREATE TABLE doctor (
    doctor_id INT PRIMARY KEY AUTO_INCREMENT,
    username VARCHAR(50) UNIQUE NOT NULL,
    password_hash VARCHAR(255) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    full_name VARCHAR(100) NOT NULL,
    specialization VARCHAR(100),
    license_number VARCHAR(50) UNIQUE,
    phone_number VARCHAR(20),
    years_of_experience INT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Patient Table
CREATE TABLE patient (
    patient_id INT PRIMARY KEY AUTO_INCREMENT,
    username VARCHAR(50) UNIQUE NOT NULL,
    password_hash VARCHAR(255) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    full_name VARCHAR(100) NOT NULL,
    date_of_birth DATE,
    gender ENUM('Male', 'Female', 'Other'),
    phone_number VARCHAR(20),
    emergency_contact VARCHAR(20),
    blood_type VARCHAR(5),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Appointment Table
CREATE TABLE appointment (
    appointment_id INT PRIMARY KEY AUTO_INCREMENT,
    patient_id INT NOT NULL,
    doctor_id INT NOT NULL,
    appointment_date DATE NOT NULL,
    appointment_time TIME NOT NULL,
    status ENUM('Scheduled', 'Completed', 'Cancelled', 'No-show') DEFAULT 'Scheduled',
    reason_for_visit TEXT,
    notes TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (patient_id) REFERENCES patient(patient_id),
    FOREIGN KEY (doctor_id) REFERENCES doctor(doctor_id)
);

-- Doctor Availability Table
CREATE TABLE doctor_available_times (
    availability_id INT PRIMARY KEY AUTO_INCREMENT,
    doctor_id INT NOT NULL,
    day_of_week ENUM('Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday'),
    start_time TIME NOT NULL,
    end_time TIME NOT NULL,
    FOREIGN KEY (doctor_id) REFERENCES doctor(doctor_id)
);
```

### **MongoDB Collections (NoSQL Data)**
```javascript
// Prescriptions Collection
db.createCollection("prescriptions", {
    validator: {
        $jsonSchema: {
            bsonType: "object",
            required: ["patient_id", "doctor_id", "medications", "issue_date"],
            properties: {
                patient_id: { bsonType: "int" },
                doctor_id: { bsonType: "int" },
                appointment_id: { bsonType: "int" },
                medications: {
                    bsonType: "array",
                    items: {
                        bsonType: "object",
                        required: ["name", "dosage", "frequency"],
                        properties: {
                            name: { bsonType: "string" },
                            dosage: { bsonType: "string" },
                            frequency: { bsonType: "string" },
                            duration: { bsonType: "string" },
                            instructions: { bsonType: "string" }
                        }
                    }
                },
                issue_date: { bsonType: "date" },
                expiry_date: { bsonType: "date" },
                refills_remaining: { bsonType: "int" },
                pharmacy_notes: { bsonType: "string" }
            }
        }
    }
});

// Medical Records Collection
db.createCollection("medical_records", {
    validator: {
        $jsonSchema: {
            bsonType: "object",
            required: ["patient_id", "record_date"],
            properties: {
                patient_id: { bsonType: "int" },
                record_date: { bsonType: "date" },
                vital_signs: {
                    bsonType: "object",
                    properties: {
                        blood_pressure: { bsonType: "string" },
                        heart_rate: { bsonType: "int" },
                        temperature: { bsonType: "double" },
                        weight: { bsonType: "double" },
                        height: { bsonType: "double" }
                    }
                },
                diagnosis: { bsonType: "string" },
                treatment_plan: { bsonType: "string" },
                lab_results: { bsonType: "array" },
                imaging_reports: { bsonType: "array" }
            }
        }
    }
});
```

## 🔐 Security Implementation

### **JWT Authentication Flow**
```java
// TokenService.java
@Service
public class TokenService {
    
    @Value("${jwt.secret}")
    private String secretKey;
    
    @Value("${jwt.expiration}")
    private long expirationTime;
    
    public String generateToken(UserDetails userDetails) {
        Map<String, Object> claims = new HashMap<>();
        claims.put("role", userDetails.getAuthorities().iterator().next().getAuthority());
        claims.put("userId", ((CustomUserDetails) userDetails).getUserId());
        
        return Jwts.builder()
                .setClaims(claims)
                .setSubject(userDetails.getUsername())
                .setIssuedAt(new Date(System.currentTimeMillis()))
                .setExpiration(new Date(System.currentTimeMillis() + expirationTime))
                .signWith(SignatureAlgorithm.HS512, secretKey)
                .compact();
    }
    
    public boolean validateToken(String token, UserDetails userDetails) {
        final String username = extractUsername(token);
        return (username.equals(userDetails.getUsername()) && !isTokenExpired(token));
    }
}

// SecurityConfig.java
@Configuration
@EnableWebSecurity
public class SecurityConfig {
    
    @Bean
    public SecurityFilterChain securityFilterChain(HttpSecurity http) throws Exception {
        http
            .csrf(AbstractHttpConfigurer::disable)
            .authorizeHttpRequests(auth -> auth
                .requestMatchers("/api/auth/**").permitAll()
                .requestMatchers("/api/admin/**").hasRole("ADMIN")
                .requestMatchers("/api/doctor/**").hasRole("DOCTOR")
                .requestMatchers("/api/patient/**").hasRole("PATIENT")
                .anyRequest().authenticated()
            )
            .sessionManagement(session -> session
                .sessionCreationPolicy(SessionCreationPolicy.STATELESS)
            )
            .addFilterBefore(jwtAuthenticationFilter(), UsernamePasswordAuthenticationFilter.class);
        
        return http.build();
    }
}
```

## 🧪 API Endpoints

### **Authentication**
| Method | Endpoint | Description | Auth Required |
|--------|----------|-------------|---------------|
| POST | `/api/auth/login` | User login | No |
| POST | `/api/auth/register` | User registration | No |
| POST | `/api/auth/refresh` | Refresh JWT token | Yes |
| POST | `/api/auth/logout` | User logout | Yes |

### **Appointment Management**
| Method | Endpoint | Description | Role |
|--------|----------|-------------|------|
| GET | `/api/appointments` | Get all appointments | ADMIN |
| GET | `/api/appointments/doctor/{id}` | Get doctor's appointments | DOCTOR |
| GET | `/api/appointments/patient/{id}` | Get patient's appointments | PATIENT |
| POST | `/api/appointments` | Create new appointment | PATIENT |
| PUT | `/api/appointments/{id}` | Update appointment | DOCTOR/PATIENT |
| DELETE | `/api/appointments/{id}` | Cancel appointment | DOCTOR/PATIENT |
| GET | `/api/appointments/available/{doctorId}/{date}` | Get available slots | PATIENT |

### **Prescription Management**
| Method | Endpoint | Description | Role |
|--------|----------|-------------|------|
| GET | `/api/prescriptions/patient/{id}` | Get patient prescriptions | DOCTOR/PATIENT |
| POST | `/api/prescriptions` | Create prescription | DOCTOR |
| PUT | `/api/prescriptions/{id}` | Update prescription | DOCTOR |
| DELETE | `/api/prescriptions/{id}` | Delete prescription | DOCTOR |
| GET | `/api/prescriptions/history/{patientId}` | Prescription history | DOCTOR |

## 🐳 Docker Deployment

### **Multi-Container Setup**
```yaml
# docker-compose.yml
version: '3.8'

services:
  mysql:
    image: mysql:8.0
    container_name: cms-mysql
    environment:
      MYSQL_ROOT_PASSWORD: rootpassword
      MYSQL_DATABASE: cms
      MYSQL_USER: cms_user
      MYSQL_PASSWORD: cms_password
    ports:
      - "3306:3306"
    volumes:
      - mysql_data:/var/lib/mysql
      - ./SQL:/docker-entrypoint-initdb.d
    networks:
      - clinic-network

  mongodb:
    image: mongo:7.0
    container_name: cms-mongodb
    environment:
      MONGO_INITDB_ROOT_USERNAME: root
      MONGO_INITDB_ROOT_PASSWORD: mongopassword
      MONGO_INITDB_DATABASE: prescriptions
    ports:
      - "27017:27017"
    volumes:
      - mongodb_data:/data/db
      - ./prescriptions/mongodb-init.js:/docker-entrypoint-initdb.d/mongodb-init.js
    networks:
      - clinic-network

  backend:
    build: .
    container_name: cms-backend
    environment:
      SPRING_DATASOURCE_URL: jdbc:mysql://mysql:3306/cms
      SPRING_DATASOURCE_USERNAME: cms_user
      SPRING_DATASOURCE_PASSWORD: cms_password
      SPRING_DATA_MONGODB_URI: mongodb://root:mongopassword@mongodb:27017/prescriptions?authSource=admin
      JWT_SECRET: your-secret-key-change-in-production
    ports:
      - "8080:8080"
    depends_on:
      - mysql
      - mongodb
    networks:
      - clinic-network

  adminer:
    image: adminer:latest
    container_name: cms-adminer
    ports:
      - "8081:8080"
    networks:
      - clinic-network

networks:
  clinic-network:
    driver: bridge

volumes:
  mysql_data:
  mongodb_data:
```

### **Backend Dockerfile**
```dockerfile
# Dockerfile
FROM eclipse-temurin:17-jdk-alpine

WORKDIR /app

# Copy Maven wrapper and pom.xml
COPY mvnw .
COPY .mvn .mvn
COPY pom.xml .

# Download dependencies
RUN ./mvnw dependency:go-offline -B

# Copy source code
COPY src src

# Build application
RUN ./mvnw clean package -DskipTests

# Create non-root user
RUN addgroup -S spring && adduser -S spring -G spring
USER spring:spring

# Run application
ENTRYPOINT ["java", "-jar", "target/back-end-0.0.1-SNAPSHOT.jar"]

# Health check
HEALTHCHECK --interval=30s --timeout=3s --start-period=5s --retries=3 \
  CMD curl -f http://localhost:8080/actuator/health || exit 1
```

## 🤖 CI/CD Pipeline

### **GitHub Actions Workflow**
```yaml
# .github/workflows/deploy-production.yml
name: Deploy to Production

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  build-and-test:
    runs-on: ubuntu-latest
    
    services:
      mysql:
        image: mysql:8.0
        env:
          MYSQL_ROOT_PASSWORD: root
          MYSQL_DATABASE: cms
        options: >-
          --health-cmd="mysqladmin ping"
          --health-interval=10s
          --health-timeout=5s
          --health-retries=3
        ports:
          - 3306:3306
      
      mongodb:
        image: mongo:7.0
        env:
          MONGO_INITDB_ROOT_USERNAME: root
          MONGO_INITDB_ROOT_PASSWORD: mongopassword
        ports:
          - 27017:27017
    
    steps:
    - uses: actions/checkout@v4
    
    - name: Set up JDK 17
      uses: actions/setup-java@v4
      with:
        java-version: '17'
        distribution: 'temurin'
    
    - name: Build with Maven
      run: mvn clean compile
    
    - name: Run tests
      run: mvn test
    
    - name: SonarCloud Scan
      uses: SonarSource/sonarcloud-github-action@master
      env:
        GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        SONAR_TOKEN: ${{ secrets.SONAR_TOKEN }}
    
    - name: Build Docker image
      run: docker build -t clinic-management-system:latest .
    
    - name: Run integration tests
      run: |
        docker-compose -f docker-compose.test.yml up -d
        sleep 30
        mvn verify -P integration-test
        docker-compose -f docker-compose.test.yml down
    
    - name: Deploy to Production
      if: github.ref == 'refs/heads/main'
      run: |
        echo "${{ secrets.DOCKER_PASSWORD }}" | docker login -u "${{ secrets.DOCKER_USERNAME }}" --password-stdin
        docker tag clinic-management-system:latest ${{ secrets.DOCKER_USERNAME }}/clinic-management-system:latest
        docker push ${{ secrets.DOCKER_USERNAME }}/clinic-management-system:latest
```

## 📊 Advanced Features

### **Stored Procedures for Analytics**
```sql
-- GetDailyAppointmentReportByDoctor.sql
DELIMITER $$
CREATE PROCEDURE GetDailyAppointmentReportByDoctor(
    IN doctorId INT,
    IN reportDate DATE
)
BEGIN
    SELECT 
        a.appointment_id,
        p.full_name AS patient_name,
        a.appointment_time,
        a.status,
        a.reason_for_visit,
        TIMESTAMPDIFF(MINUTE, 
            CONCAT(a.appointment_date, ' ', a.appointment_time),
            NOW()) AS minutes_until_appointment
    FROM appointment a
    JOIN patient p ON a.patient_id = p.patient_id
    WHERE a.doctor_id = doctorId 
        AND a.appointment_date = reportDate
    ORDER BY a.appointment_time;
END$$
DELIMITER ;

-- GetDoctorWithMostPatientsByMonth.sql
DELIMITER $$
CREATE PROCEDURE GetDoctorWithMostPatientsByMonth(
    IN month INT,
    IN year INT
)
BEGIN
    SELECT 
        d.doctor_id,
        d.full_name,
        d.specialization,
        COUNT(DISTINCT a.patient_id) AS unique_patients,
        COUNT(a.appointment_id) AS total_appointments
    FROM doctor d
    LEFT JOIN appointment a ON d.doctor_id = a.doctor_id
        AND MONTH(a.appointment_date) = month
        AND YEAR(a.appointment_date) = year
    GROUP BY d.doctor_id, d.full_name, d.specialization
    ORDER BY unique_patients DESC, total_appointments DESC
    LIMIT 5;
END$$
DELIMITER ;
```

### **Real-time Notifications**
```java
// WebSocket configuration for real-time updates
@Configuration
@EnableWebSocketMessageBroker
public class WebSocketConfig implements WebSocketMessageBrokerConfigurer {
    
    @Override
    public void configureMessageBroker(MessageBrokerRegistry config) {
        config.enableSimpleBroker("/topic", "/queue");
        config.setApplicationDestinationPrefixes("/app");
    }
    
    @Override
    public void registerStompEndpoints(StompEndpointRegistry registry) {
        registry.addEndpoint("/ws-clinic")
                .setAllowedOriginPatterns("*")
                .withSockJS();
    }
}

// Appointment notification service
@Service
public class NotificationService {
    
    @Autowired
    private SimpMessagingTemplate messagingTemplate;
    
    public void sendAppointmentNotification(String userId, Appointment appointment) {
        NotificationMessage message = NotificationMessage.builder()
                .type("APPOINTMENT_REMINDER")
                .title("Appointment Reminder")
                .content(String.format(
                    "You have an appointment with Dr. %s at %s",
                    appointment.getDoctor().getFullName(),
                    appointment.getAppointmentTime()
                ))
                .timestamp(new Date())
                .build();
        
        messagingTemplate.convertAndSendToUser(
            userId,
            "/queue/notifications",
            message
        );
    }
}
```

## 🧪 Testing Strategy

### **Unit Tests**
```java
// AppointmentServiceTest.java
@ExtendWith(MockitoExtension.class)
class AppointmentServiceTest {
    
    @Mock
    private AppointmentRepository appointmentRepository;
    
    @Mock
    private DoctorRepository doctorRepository;
    
    @Mock
    private PatientRepository patientRepository;
    
    @InjectMocks
    private AppointmentService appointmentService;
    
    @Test
    void createAppointment_Success() {
        // Arrange
        AppointmentDTO appointmentDTO = new AppointmentDTO();
        appointmentDTO.setPatientId(1);
        appointmentDTO.setDoctorId(1);
        appointmentDTO.setAppointmentDate(LocalDate.now().plusDays(1));
        appointmentDTO.setAppointmentTime(LocalTime.of(10, 0));
        
        Patient patient = new Patient();
        patient.setPatientId(1);
        
        Doctor doctor = new Doctor();
        doctor.setDoctorId(1);
        
        when(patientRepository.findById(1)).thenReturn(Optional.of(patient));
        when(doctorRepository.findById(1)).thenReturn(Optional.of(doctor));
        when(appointmentRepository.save(any(Appointment.class)))
            .thenAnswer(invocation -> invocation.getArgument(0));
        
        // Act
        Appointment result = appointmentService.createAppointment(appointmentDTO);
        
        // Assert
        assertNotNull(result);
        assertEquals(AppointmentStatus.SCHEDULED, result.getStatus());
        verify(appointmentRepository, times(1)).save(any(Appointment.class));
    }
}
```

### **Integration Tests**
```java
// AppointmentControllerIntegrationTest.java
@SpringBootTest
@AutoConfigureMockMvc
@Testcontainers
class AppointmentControllerIntegrationTest {
    
    @Container
    static MySQLContainer<?> mysql = new MySQLContainer<>("mysql:8.0")
            .withDatabaseName("cms_test")
            .withUsername("test")
            .withPassword("test");
    
    @Container
    static MongoDBContainer mongo = new MongoDBContainer("mongo:7.0");
    
    @DynamicPropertySource
    static void configureProperties(DynamicPropertyRegistry registry) {
        registry.add("spring.datasource.url", mysql::getJdbcUrl);
        registry.add("spring.datasource.username", mysql::getUsername);
        registry.add("spring.datasource.password", mysql::getPassword);
        registry.add("spring.data.mongodb.uri", mongo::getReplicaSetUrl);
    }
    
    @Test
    @WithMockUser(username = "patient1", roles = "PATIENT")
    void createAppointment_ValidRequest_ReturnsCreated() throws Exception {
        // Test implementation
    }
}
```

## 📈 Performance Optimization

### **Database Indexing Strategy**
```sql
-- Optimized indexes for frequent queries
CREATE INDEX idx_appointment_doctor_date 
ON appointment(doctor_id, appointment_date, appointment_time);

CREATE INDEX idx_appointment_patient_status 
ON appointment(patient_id, status, appointment_date DESC);

CREATE INDEX idx_doctor_specialization 
ON doctor(specialization, years_of_experience DESC);

CREATE INDEX idx_patient_name 
ON patient(full_name, date_of_birth);

-- MongoDB indexes
db.appointments.createIndex({ doctor_id: 1, appointment_date: 1 });
db.prescriptions.createIndex({ patient_id: 1, issue_date: -1 });
db.medical_records.createIndex({ patient_id: 1, record_date: -1 });
```

### **Caching Strategy**
```java
// Redis caching configuration
@Configuration
@EnableCaching
public class CacheConfig {
    
    @Bean
    public RedisCacheManager cacheManager(RedisConnectionFactory connectionFactory) {
        RedisCacheConfiguration config = RedisCacheConfiguration.defaultCacheConfig()
                .entryTtl(Duration.ofMinutes(10))
                .disableCachingNullValues()
                .serializeValuesWith(RedisSerializationContext.SerializationPair
                    .fromSerializer(new GenericJackson2JsonRedisSerializer()));
        
        return RedisCacheManager.builder(connectionFactory)
                .cacheDefaults(config)
                .withInitialCacheConfigurations(cacheConfigurations())
                .transactionAware()
                .build();
    }
    
    private Map<String, RedisCacheConfiguration> cacheConfigurations() {
        Map<String, RedisCacheConfiguration> configMap = new HashMap<>();
        configMap.put("doctors", RedisCacheConfiguration.defaultCacheConfig()
                .entryTtl(Duration.ofMinutes(30)));
        configMap.put("patients", RedisCacheConfiguration.defaultCacheConfig()
                .entryTtl(Duration.ofMinutes(60)));
        return configMap;
    }
}
```

## 🚀 Deployment Options

### **Option 1: Docker Compose (Development)**
```bash
# Clone and deploy
git clone https://github.com/Willie-Conway/java-database-capstone.git
cd java-database-capstone

# Start all services
docker-compose up -d

# View logs
docker-compose logs -f backend

# Access services
# Application: http://localhost:8080
# Database Admin: http://localhost:8081
```

### **Option 2: Kubernetes (Production)**
```yaml
# kubernetes/deployment.yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: clinic-management-system
spec:
  replicas: 3
  selector:
    matchLabels:
      app: clinic-system
  template:
    metadata:
      labels:
        app: clinic-system
    spec:
      containers:
      - name: backend
        image: willieconway/clinic-management-system:latest
        ports:
        - containerPort: 8080
        env:
        - name: SPRING_PROFILES_ACTIVE
          value: "production"
        resources:
          requests:
            memory: "512Mi"
            cpu: "250m"
          limits:
            memory: "1Gi"
            cpu: "500m"
        livenessProbe:
          httpGet:
            path: /actuator/health
            port: 8080
          initialDelaySeconds: 60
          periodSeconds: 10
        readinessProbe:
          httpGet:
            path: /actuator/health
            port: 8080
          initialDelaySeconds: 30
          periodSeconds: 5
```

## 📚 Documentation

### **API Documentation**
- **Swagger UI**: http://localhost:8080/swagger-ui.html
- **OpenAPI Spec**: http://localhost:8080/v3/api-docs
- **Postman Collection**: `/docs/postman-collection.json`

### **Database Documentation**
- **ER Diagrams**: `/docs/er-diagrams/`
- **Schema Documentation**: `/docs/database-schema.md`
- **Data Dictionary**: `/docs/data-dictionary.xlsx`

### **Architecture Documentation**
- **System Architecture**: `/docs/architecture/`
- **Deployment Guide**: `/docs/deployment-guide.md`
- **Security Overview**: `/docs/security-overview.md`

## 🤝 Contributing

We welcome contributions! Please follow these guidelines:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Commit your changes**
   ```bash
   git commit -m 'Add amazing feature'
   ```
4. **Push to the branch**
   ```bash
   git push origin feature/amazing-feature
   ```
5. **Open a Pull Request**

### **Development Guidelines**
- Follow Java coding conventions
- Write comprehensive unit tests
- Update documentation for new features
- Ensure backward compatibility
- Run all tests before submitting PR

## 🐛 Troubleshooting

### **Common Issues**

1. **Database Connection Failed**
   ```bash
   # Check MySQL service
   sudo systemctl status mysql
   
   # Check MongoDB service
   sudo systemctl status mongod
   
   # Verify credentials in application.properties
   ```

2. **Port Already in Use**
   ```bash
   # Find process using port 8080
   sudo lsof -i :8080
   
   # Kill process
   sudo kill -9 <PID>
   ```

3. **Build Failures**
   ```bash
   # Clean Maven build
   mvn clean install
   
   # Clear dependency cache
   rm -rf ~/.m2/repository/com/project
   ```

4. **Docker Issues**
   ```bash
   # Rebuild containers
   docker-compose down
   docker-compose build --no-cache
   docker-compose up -d
   ```

## 📞 Support

- **GitHub Issues**: [Report Bugs](https://github.com/Willie-Conway/java-database-capstone/issues)
- **Documentation**: [Wiki](https://github.com/Willie-Conway/java-database-capstone/wiki)
- **Email**: willie.conway@example.com

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

## 🙏🏿 Acknowledgments

- **Meta Java Development Program** for curriculum and guidance
- **Spring Boot Community** for amazing framework
- **Docker Team** for containerization tools
- **All Contributors** who helped improve this project

## 🏆 Project Achievements

✅ **Full-stack Java Spring Boot application** with microservices architecture  
✅ **Multi-database integration** (MySQL + MongoDB)  
✅ **JWT-based authentication** with role-based authorization  
✅ **Complete CI/CD pipeline** with GitHub Actions  
✅ **Docker containerization** with multi-service orchestration  
✅ **Comprehensive testing suite** (Unit, Integration, E2E)  
✅ **Production-ready deployment** configurations  
✅ **Detailed documentation** and API specifications  

---

**Happy Coding! 👨🏿‍💻 Let's revolutionize healthcare technology together! 🏥✨**

*Project Completed: Jan 20, 2024*  
*Last Updated: Jan 28, 2025*  
*Java Version: 17*  
*Spring Boot Version: 3.2.0*  
*MySQL Version: 8.0*  
*MongoDB Version: 7.0*
