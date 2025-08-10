# Areas and Employees System with MVC + Velocity + SQL2o

## 📌 Objective
This exercise builds upon the work from **Exercise 1**, introducing **Velocity** as a template engine and combining the **MVC** architecture with a **REST** approach to create web microservices.

The database model for areas and employees remains the same, but now dynamic views are provided through `.vtl` files, and REST routes are exposed for interacting with the data.

---

## 🛠 Tools & Requirements
- **Java**
- **Spark Java**
- **Velocity** (template engine)
- **SQL2o**
- **MySQL** (or any compatible database engine)
- Base project from **Exercise 1**
- **MVC** pattern implemented
- Environment configured according to Part III of the lab instructions

---

## 🗄 Database Model

### Tables
The data model from Exercise 1 is reused:

**AREA**
| Field   | Type     | Description                  |
|---------|----------|------------------------------|
| codigo  | PK, int  | Unique area identifier        |
| nombre  | varchar  | Area name                     |
| director| varchar  | Area director                 |

**EMPLOYEE**
| Field     | Type       | Description                              |
|-----------|------------|------------------------------------------|
| nombre    | PK, varchar| Employee name                            |
| categoria | varchar    | Employee category                        |
| dedicacion| varchar    | Dedication (e.g., full-time)              |
| codigo    | FK, int    | Area in which the employee works (ref AREA)|

---

## 📋 Implemented Features
1. **Return all areas**  
2. **Given an area, display its employees**  
3. **Add a new area**  
4. **List all employees**  
5. **Search for an employee and display their area**  
6. **Get the number of employees per area**  
7. **Add a new employee specifying their area (only one area)**  

> **Note**: A **single cohesive `.vtl` file** is built to handle the display of all functionalities instead of one file per result.

---

## 🚀 How to Run
1. **Clone the repository**
   ```bash
   git clone https://github.com/username/repo-name.git

