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

Alternatively, open your MySQL client and run the commands from hotel_management.sql manually.

The script creates a database called hotel_db and all required tables with constraints.

## ERD Description

### Entities:

**Guests**

- guest_id (PK)  
- first_name  
- last_name  
- email  
- phone  
- address  

**RoomTypes**

- room_type_id (PK)  
- type_name  
- description  
- price_per_night  

**Rooms**

- room_id (PK)  
- room_number  
- room_type_id (FK → RoomTypes.room_type_id)  
- is_available  

**Bookings**

- booking_id (PK)  
- guest_id (FK → Guests.guest_id)  
- room_id (FK → Rooms.room_id)  
- check_in  
- check_out  
- number_of_guests  
- booking_date  
- status  

**Services**

- service_id (PK)  
- service_name  
- description  
- price  

**BookingServices** (Join table for many-to-many between Bookings and Services)

- booking_id (FK → Bookings.booking_id)  
- service_id (FK → Services.service_id)  
- quantity  

### Relationships:

- Guests (1) → (M) Bookings  
- RoomTypes (1) → (M) Rooms  
- Rooms (1) → (M) Bookings  
- Bookings (M) → (M) Services (through BookingServices)



Entity-Relationship Diagram


Below is a visual representation of the database schema showing entities and their relationships:
<img width="814" height="1500" alt="hotelmanagement drawio" src="https://github.com/user-attachments/assets/22fd22c4-ff1e-46a3-ba29-b9629eda255d" />


