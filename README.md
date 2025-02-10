
# Bus Management System

A comprehensive and user-friendly **Bus Management System** developed using **Java Swing** for the graphical user interface (GUI) and integrated with **MySQL** for database management. This system allows for efficient management of bus schedules, routes, and passenger information, aiming to improve the overall functionality and ease of use for administrators.

## 🚀 Features

- **Bus Route Management**: Add, update, delete, and view bus routes, including bus details like route number, source, destination, and timings.
- **Passenger Management**: Manage passenger information with an intuitive interface to add, update, and remove passenger details.
- **Ticket Booking**: Seamless ticket booking feature for passengers, allowing seat reservations and ticket confirmations.
- **Real-time Search**: Search for buses based on routes, timings, or availability.
- **MySQL Database Integration**: All data such as bus schedules, passenger details, and bookings are securely stored in a MySQL database.

## 🔧 Technology Stack

- **Frontend**: Java Swing
- **Backend**: Java
- **Database**: MySQL
- **IDE**: IntelliJ IDEA, Eclipse, or any Java IDE

## ⚙️ Getting Started

Follow the steps below to set up the project locally.

### 1. Prerequisites

- **Java 8** or higher
- **MySQL** Database (or XAMPP with MySQL server running)
- **JDBC** for MySQL Integration
- **Apache Maven** or **Gradle** (if using dependencies management)
  
### 2. Clone the Repository

Clone this repository to your local machine using Git:

```bash
git clone https://github.com/yourusername/bus-management-system.git
```

### 3. Set Up MySQL Database

- Install MySQL on your local machine if you haven’t already.
- Create a new database (e.g., `bus_management_system`).
- Create the necessary tables by running the SQL scripts provided in the `sql` directory. For example:

```sql
CREATE TABLE buses (
    bus_id INT AUTO_INCREMENT PRIMARY KEY,
    bus_number VARCHAR(50),
    route VARCHAR(100),
    capacity INT,
    available_seats INT
);

CREATE TABLE passengers (
    passenger_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    phone_number VARCHAR(15),
    ticket_id INT
);

CREATE TABLE tickets (
    ticket_id INT AUTO_INCREMENT PRIMARY KEY,
    bus_id INT,
    passenger_id INT,
    seat_number INT,
    booking_time TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (bus_id) REFERENCES buses(bus_id),
    FOREIGN KEY (passenger_id) REFERENCES passengers(passenger_id)
);
```

### 4. Database Configuration

- Open the `DatabaseConfig.java` file located in the `src/config/` folder.
- Update the following variables with your MySQL configuration:

```java
public static final String DB_URL = "jdbc:mysql://localhost:3306/bus_management_system";
public static final String USER = "root";
public static final String PASSWORD = "yourpassword";
```

### 5. Running the Application

- Open the project in your preferred Java IDE (e.g., IntelliJ IDEA, Eclipse).
- Run the main class `BusManagementSystem.java` to start the application.
- The GUI will open, and you can begin managing buses, passengers, and bookings.

## 📷 Screenshots

![image](https://github.com/user-attachments/assets/000fa21c-38ca-42a5-82a4-d2efd1f0b0fa)


## 🛠️ Key Features

### **Java Swing GUI**

- Interactive interface with intuitive navigation.
- Customizable and dynamic forms for adding, updating, and deleting records.
- Real-time display of buses and passenger information.

### **MySQL Integration**

- Data persistence with MySQL, enabling consistent and secure data management.
- CRUD operations (Create, Read, Update, Delete) for all data entities.

### **User-friendly Interface**

- Simple, easy-to-use GUI that even non-technical users can navigate with ease.
- Features like automatic error handling and input validation to ensure smooth operations.

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Contributors

- [SHAIK TASLEEM KHAN](https://github.com/Tasleemkhan7)
- [IMMANI RAMA VENKATA SRI SAI](https://github.com/saiimmani)
- [KALEPU NEERAJ TEJA](https://github.com/neerajteja17)
- [MANDA UJWAL REDDY](https://github.com/Ujwal4455)
## 🤝 Support

If you encounter any issues or need assistance with the project, feel free to open an issue in the repository or reach out to the contributors.

---
