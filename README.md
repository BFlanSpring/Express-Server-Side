# Lunchly

Lunchly is an application for managing reservations and customers for a restaurant.

- [Project Structure](#project-structure)
- [Usage](#usage)
  - [Installation](#installation)
  - [Running the App](#running-the-app)
  - [Routes](#routes)
- [Models](#models)
  - [Customer Model (`customer.js`)](#customer-model-customerjs)
  - [Reservation Model (`reservation.js`)](#reservation-model-reservationjs)
- [Database Schema](#database-schema)
- [Sample Data](#sample-data)
- [Dependencies](#dependencies)
- [Error Handling](#error-handling)
- [Contributing](#contributing)
- [License](#license)

## Project Structure

### Files

- `app.js`: Express app for Lunchly
- `customer.js`: Customer model for Lunchly
- `reservation.js`: Reservation model for Lunchly
- `data.sql`: SQL file containing sample data and table schemas

### Description

The application consists of an Express app (`app.js`) that utilizes `customer.js` and `reservation.js` models to manage customers and reservations in a restaurant. The database schema is provided in `data.sql`.

## Usage

### Installation

1. Clone this repository.
2. Install dependencies using `npm install`.
3. Create a PostgreSQL database and configure the connection in `db.js`.

### Running the App

Run the application using `npm start`. By default, it runs on `http://localhost:3000`.

### Routes

- `/customers`: Manages customers
- `/reservations`: Manages reservations
- Error routes: Handle 404 and general errors

## Models

### Customer Model (`customer.js`)

- Represents a customer of the restaurant
- Methods:
  - `all()`: Retrieve all customers
  - `get(id)`: Retrieve a customer by ID
  - `getReservations()`: Get all reservations for a customer
  - `save()`: Save or update a customer

### Reservation Model (`reservation.js`)

- Represents a reservation for a party
- Methods:
  - `getReservationsForCustomer(customerId)`: Retrieve reservations for a customer
  - `save()`: Save or update a reservation

## Database Schema

- `customers`: Stores customer information
- `reservations`: Stores reservation details

## Sample Data

Sample data for customers and reservations is available in `data.sql`.

## Dependencies

- `express`: Web framework for Node.js
- `nunjucks`: Templating engine
- `body-parser`: Middleware to parse HTTP request body

## Error Handling

The app includes error handling for 404 (Not Found) and general errors.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request.

## License

This project is meant for open source use by all!!!!
