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

Store and manage aircraft details (model, tail number, capacity)
Add and track pilot information (pilot ID, name, license number, experience)
Log flight details such as:
Flight ID
Pilot ID
Aircraft ID
Departure airport
Arrival airport
Departure time
Arrival time

Supports CRUD operations (Create, Read, Update, Delete)
Designed with normalized table structure
Can be used by any SQL engine (SQLite, MySQL, MariaDB,Command prompt)

🛠️ Technologies / Tools Used

Command Prompt (CMD) for database creation and queries
SQL (Structured Query Language)
Git & GitHub for version control and repository hosting

📥 Steps to Install & Run the Project

1. Install SQLite or MySQL
If using SQLite, download from the official website and place sqlite3.exe in your working folder.
If using MySQL, install MySQL Community Server.

2. Create the Database
In CMD, run:
sqlite3 flight_log.db
or for MySQL:
mysql -u root -p
CREATE DATABASE flight_log;
USE flight_log;

3. Create the Tables
Run:
CREATE TABLE aircraft (
  aircraft_id INT AUTO_INCREMENT PRIMARY KEY,
  model VARCHAR(100) NOT NULL,
  tail_number VARCHAR(20) UNIQUE NOT NULL,
  capacity INT NOT NULL
); 

CREATE TABLE pilots (
  pilot_id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  license_number VARCHAR(50) UNIQUE NOT NULL,
  experience_years INT NOT NULL
);

CREATE TABLE flights (
  flight_id INT AUTO_INCREMENT PRIMARY KEY,
  pilot_id INT,
  aircraft_id INT,
  departure_airport VARCHAR(50),
  arrival_airport VARCHAR(50),
  departure_time DATETIME,
  arrival_time DATETIME,
  FOREIGN KEY (pilot_id) REFERENCES pilots(pilot_id),
  FOREIGN KEY (aircraft_id) REFERENCES aircraft(aircraft_id)
);

4. Insert Sample Data
Example:
INSERT INTO aircraft (model, tail_number, capacity)
VALUES 
('Airbus A320', 'VT-AT1', 180),
('Boeing 737', 'VT-B73', 160);
(You can add pilots and flights similarly.)
5. Run Queries

Examples:

SELECT * FROM flights;
SELECT pilot_id, name FROM pilots;

6. Close the Database

.exit


---

🧪 Instructions for Testing

To make sure your project works properly:

✔ Test 1: Retrieve All Aircraft

SELECT * FROM aircraft;

✔ Test 2: Retrieve All Pilots

SELECT * FROM pilots;

✔ Test 3: Join Table Test

SELECT flights.flight_id, pilots.name, aircraft.model
FROM flights
JOIN pilots ON flights.pilot_id = pilots.pilot_id
JOIN aircraft ON flights.aircraft_id = aircraft.aircraft_id;

✔ Test 4: Add a New Flight

Insert data and confirm using:

SELECT * FROM flights;

✔ Test 5: Check Foreign Key Relations

Try inserting invalid pilot or aircraft IDs and verify errors.


---

📸 Screenshots (Optional)

You may include:

CMD screenshot of table creation

Screenshot of SELECT * FROM flights;

Screenshot of your GitHub repository



---

If you want, I can create a full README.md file for your GitHub (download-ready).
