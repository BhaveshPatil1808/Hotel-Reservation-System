<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hotel Reservation System - README</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 40px;
            padding: 20px;
            background-color: #f4f4f4;
        }
        h1, h2 {
            color: #333;
        }
        pre {
            background: #eee;
            padding: 10px;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <h1>Hotel Reservation System</h1>
    
    <h2>Overview</h2>
    <p>The <strong>Hotel Reservation System</strong> is a Java-based console application that allows users to manage hotel room reservations. The application connects to a MySQL database to store and retrieve reservation data.</p>
    
    <h2>Features</h2>
    <ul>
        <li><strong>Reserve a Room:</strong> Add a new reservation with guest details and room number.</li>
        <li><strong>View Reservations:</strong> Display all current reservations.</li>
        <li><strong>Get Room Number:</strong> Retrieve room details based on reservation ID and guest name.</li>
        <li><strong>Update Reservation:</strong> Modify guest name, room number, and contact details.</li>
        <li><strong>Delete Reservation:</strong> Remove an existing reservation.</li>
    </ul>
    
    <h2>Prerequisites</h2>
    <p>To run this application, ensure you have the following installed:</p>
    <ul>
        <li><strong>Java Development Kit (JDK) 8 or higher</strong></li>
        <li><strong>MySQL Database</strong></li>
        <li><strong>MySQL JDBC Driver</strong> (Connector/J)</li>
    </ul>
    
    <h2>Database Setup</h2>
    <pre>
CREATE DATABASE hotel_db;
USE hotel_db;
CREATE TABLE reservations (
    reservation_id INT AUTO_INCREMENT PRIMARY KEY,
    guest_name VARCHAR(100) NOT NULL,
    room_number INT NOT NULL,
    contact_number VARCHAR(20) NOT NULL,
    reservation_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
    </pre>
    
    <h2>How to Run</h2>
    <ol>
        <li>Compile the Java program:
            <pre>javac HotelReservationSystem.java</pre>
        </li>
        <li>Run the program:
            <pre>java HotelReservationSystem</pre>
        </li>
        <li>Follow the on-screen menu to interact with the system.</li>
    </ol>
    
    <h2>Usage</h2>
    <p>- Enter the required details such as guest name, room number, and contact number.</p>
    <p>- Use numerical inputs to navigate the menu.</p>
    <p>- Ensure that MySQL is running before launching the application.</p>
    
    <h2>Notes</h2>
    <ul>
        <li>This application uses <strong>JDBC</strong> for database connectivity.</li>
        <li>The database credentials are stored in plain text within the source code. For production use, consider using environment variables or a configuration file.</li>
        <li>The SQL queries used are vulnerable to SQL injection. Consider using <strong>PreparedStatement</strong> to enhance security.</li>
    </ul>
    
    <h2>License</h2>
    <p>This project is open-source and available for modification and distribution.</p>
    
    <h2>Author</h2>
    <p>[Your Name]</p>
</body>
</html>
