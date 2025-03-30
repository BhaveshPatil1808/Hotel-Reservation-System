Hotel Reservation System

Overview

The Hotel Reservation System is a Java-based console application that allows users to manage hotel room reservations. The application connects to a MySQL database to store and retrieve reservation data.

Features

Reserve a Room: Add a new reservation with guest details and room number.

View Reservations: Display all current reservations.

Get Room Number: Retrieve room details based on reservation ID and guest name.

Update Reservation: Modify guest name, room number, and contact details.

Delete Reservation: Remove an existing reservation.

Prerequisites

To run this application, ensure you have the following installed:

Java Development Kit (JDK) 8 or higher

MySQL Database

MySQL JDBC Driver (Connector/J)

Database Setup

Start MySQL and create a new database:

CREATE DATABASE hotel_db;

Switch to the database:

USE hotel_db;

Create the reservations table:

CREATE TABLE reservations (
    reservation_id INT AUTO_INCREMENT PRIMARY KEY,
    guest_name VARCHAR(100) NOT NULL,
    room_number INT NOT NULL,
    contact_number VARCHAR(20) NOT NULL,
    reservation_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

Update the url, username, and password variables in the Java code to match your MySQL configuration.

How to Run

Compile the Java program:

javac HotelReservationSystem.java

Run the program:

java HotelReservationSystem

Follow the on-screen menu to interact with the system.

Usage

When prompted, enter the required details such as guest name, room number, and contact number.

Use numerical inputs to navigate the menu.

Ensure that MySQL is running before launching the application.

Notes

This application uses JDBC for database connectivity.

The database credentials are stored in plain text within the source code. For production use, consider using environment variables or a configuration file.

The SQL queries used are vulnerable to SQL injection. Consider using PreparedStatement to enhance security.
