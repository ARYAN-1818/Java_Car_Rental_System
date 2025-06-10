# Car Rental Management System

A comprehensive car rental management system built to handle vehicle rentals, customer management, and booking operations efficiently.

## 🚗 Features

- **Vehicle Management**: Add, update, and manage car inventory
- **Customer Registration**: Customer account creation and profile management
- **Booking System**: Reserve vehicles with date/time selection
- **Rental Processing**: Check-out and check-in functionality
- **Payment Integration**: Handle rental payments and billing
- **Inventory Tracking**: Real-time vehicle availability status
- **Reporting**: Generate rental reports and analytics
- **Admin Dashboard**: Administrative controls and system monitoring

## 🏗️ System Architecture

### Database Layer
- **Database Schema**: Relational database design for cars, customers, bookings, and payments
- **Model Classes**:
  - `Car` - Vehicle information and specifications
  - `Customer` - Customer profile and contact details
  - `Booking` - Rental reservation records
  - `Payment` - Transaction and billing information
  - `Category` - Vehicle categories (SUV, Sedan, etc.)

### Data Access Layer (DAO Pattern)
- **CarDAO** - Vehicle data operations
- **CustomerDAO** - Customer data management
- **BookingDAO** - Booking and reservation handling
- **PaymentDAO** - Payment processing operations
- **DatabaseConnection** - Database connectivity and configuration

### Business Logic Layer
- **RentalService** - Core rental business logic
- **PaymentService** - Payment processing and validation
- **InventoryService** - Vehicle availability management
- **NotificationService** - Email/SMS notifications

### User Interface Layer
- **MainUI** - Primary application interface
- **VehicleManagementUI** - Car inventory management
- **BookingUI** - Reservation and booking interface
- **CustomerUI** - Customer management interface
- **ReportsUI** - Analytics and reporting dashboard

## 🛠️ Technologies Used

- **Programming Language**: Java 17+
- **Database**: MySQL 8.0
- **Framework**: Spring Boot 3.0
- **Frontend**: JavaFX / Swing (Desktop) or React (Web)
- **Build Tool**: Maven / Gradle
- **Testing**: JUnit 5, Mockito

## 📋 Prerequisites

- Java Development Kit (JDK) 17 or higher
- MySQL Server 8.0+
- Maven 3.6+ or Gradle 7.0+
- IDE (IntelliJ IDEA, Eclipse, or VS Code)

## 🚀 Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/car-rental-system.git
   cd car-rental-system
   ```

2. **Set up the database:**
   ```sql
   CREATE DATABASE car_rental_db;
   -- Import the provided SQL schema file
   SOURCE database/schema.sql;
   ```

3. **Configure database connection:**
   ```properties
   # Update src/main/resources/application.properties
   spring.datasource.url=jdbc:mysql://localhost:3306/car_rental_db
   spring.datasource.username=your_username
   spring.datasource.password=your_password
   ```

4. **Build and run:**
   ```bash
   # Using Maven
   mvn clean install
   mvn spring-boot:run
   
   # Using Gradle
   ./gradlew build
   ./gradlew bootRun
   ```

## 📊 Database Schema

### Core Tables
- **cars**: Vehicle information (make, model, year, license plate, etc.)
- **customers**: Customer profiles and contact information
- **bookings**: Rental reservations with dates and status
- **payments**: Transaction records and payment details
- **categories**: Vehicle categories and pricing tiers

### Relationships
- One-to-Many: Customer → Bookings
- One-to-Many: Car → Bookings
- One-to-One: Booking → Payment

## 🎯 Usage

1. **Admin Functions:**
   - Add new vehicles to inventory
   - Manage customer accounts
   - Process rentals and returns
   - Generate reports

2. **Customer Functions:**
   - Browse available vehicles
   - Make reservations
   - View booking history
   - Process payments

3. **System Features:**
   - Automated availability checking
   - Late return penalties
   - Maintenance scheduling
   - Insurance tracking

## 🧪 Testing

Run the test suite:
```bash
# Unit tests
mvn test

# Integration tests
mvn integration-test
```

## 📝 API Documentation

Access the API documentation at: `http://localhost:8080/swagger-ui.html` (if using Swagger)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -m 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Open a Pull Request

## 📁 Project Structure

```
car-rental-system/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── model/
│   │   │   ├── dao/
│   │   │   ├── service/
│   │   │   ├── ui/
│   │   │   └── config/
│   │   └── resources/
│   └── test/
├── database/
│   └── schema.sql
├── docs/
├── README.md
└── pom.xml
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- **Your Name** - *Initial work* - [YourGitHub](https://github.com/yourusername)

## 🐛 Bug Reports & Feature Requests

Please use the [GitHub Issues](https://github.com/yourusername/car-rental-system/issues) page to report bugs or request new features.

## 📞 Support

For support, email your-email@example.com or join our Slack channel.
