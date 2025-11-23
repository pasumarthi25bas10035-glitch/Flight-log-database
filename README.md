#Flight log database

📌Project Overview

The Flight Log Database is a structured SQL-based system designed to store, manage, and retrieve essential information related to flights, pilots, and aircraft.
The main purpose of this project is to build a simple yet functional aviation record-keeping system that can be used for training, learning SQL, or as the backend for an aviation management tool.

This database stores details such as:
Aircraft information
Pilot details
Flight schedules, including departure and arrival data
It is designed using SQLite / MySQL commands in CMD and follows proper relational database principles

✨ Features

1. Aircraft Management
Store details like aircraft model, tail number, and seating capacity.
Ensure unique tail numbers to avoid duplication.
Maintain a structured list of all aircraft in use.

2. Pilot Information Tracking
Record pilot details including name, license number, and years of experience.
Enforce unique license numbers for data accuracy.
Easily retrieve pilot information for assigned flights.

3. Flight Log Storage
Save complete flight details:
Flight ID
Pilot assigned to the flight
Aircraft used
Departure airport
Arrival airport
Departure time
Arrival time
Maintains a chronological history of all flights.

4. Relationship & Constraints Management
Proper foreign key relationships between pilots, aircraft, and flights.
Ensures data integrity and prevents invalid entries (such as flights without a valid pilot).

5. CRUD Operations
Create, Read, Update, and Delete:
Aircraft records
Pilot records
Flight logs
Fully functional SQL operations for database training.

6. Search & Query Support
Retrieve flights by pilot, aircraft, date, or airports.
Perform join queries to combine pilot and aircraft data with flight logs.
Useful for reporting and analytics.

7. Error Handling Through Schema Design
Unique constraints on license_number and tail_number.
Prevents incorrect or duplicate entries in the system.

8. Portable Database
Works with SQLite, MySQL, or MariaDB.
Can run via Command Prompt, Python, or any database GUI tool.

9. Lightweight & Easy to Use
Simple table structure
Beginner-friendly
Ideal for academic projects and aviation-related learning

🛠️ Technologies / Tools Used

Command Prompt (CMD) for database creation and queries
SQL (Structured Query Language)
Git & GitHub for version control and repository hosting

📥 Steps to Install & Run the Project

1. Install SQLite or MySQL
If using SQLite, download from the official website and place sqlite3.exe in your working folder.
If using MySQL, install MySQL Community Server.

2. Create the Database

3. Create the Tables

4. 
