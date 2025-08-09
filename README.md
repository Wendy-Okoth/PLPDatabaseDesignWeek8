# Hotel Management System

## Description

This project is a **Hotel Management System** database implemented using MySQL. It manages hotel operations including guests, rooms, bookings, and additional services. The database schema supports:

- Tracking guest information
- Managing different room types and their availability
- Handling room bookings with statuses
- Linking bookings to optional hotel services

The SQL script includes tables with proper primary keys, foreign keys, constraints, and many-to-many relationships where necessary.

---

## How to Setup / Run

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/Wendy-Okoth/PLPDatabaseDesignWeek8.git
   
2. Import the SQL file into your MySQL server:
   mysql -u yourusername -p < hotel_management.sql

3. Alternatively, open your MySQL client and run the commands from hotel_management.sql manually.

4. The script creates a database called hotel_db and all required tables with constraints.

5. Project Files - hotel_management.sql - Main SQL script file containing all CREATE TABLE statements and constraints, fully commented.


Entity-Relationship Diagram


Below is a visual representation of the database schema showing entities and their relationships:
<img width="814" height="1500" alt="hotelmanagement drawio" src="https://github.com/user-attachments/assets/22fd22c4-ff1e-46a3-ba29-b9629eda255d" />


