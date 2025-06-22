# airbnb-clone-project

## Project Goals

User Management: Implement a secure system for user registration, authentication, and profile management.
Property Management: Develop features for property listing creation, updates, and retrieval.
Booking System: Create a booking mechanism for users to reserve properties and manage booking details.
Payment Processing: Integrate a payment system to handle transactions and record payment details.
Review System: Allow users to leave reviews and ratings for properties.
Data Optimization: Ensure efficient data retrieval and storage through database optimizations

## Team Roles

Backend Developer: Responsible for implementing API endpoints, database schemas, and business logic.
Database Administrator: Manages database design, indexing, and optimizations.
DevOps Engineer: Handles deployment, monitoring, and scaling of the backend services. Facilitates cooperation between development and operations teams. Builds continuous integration and continuous delivery (CI/CD) pipelines for faster delivery
QA Engineer: Ensures the backend functionalities are thoroughly tested and meet quality standards. Makes sure an application performs according to requirements. Spots functional and non-functional defects

## Technology Stack

Django: A high-level Python web framework used for building the RESTful API.
Django REST Framework: Provides tools for creating and managing RESTful APIs.
PostgreSQL: A powerful relational database used for data storage.
GraphQL: Allows for flexible and efficient querying of data.
Celery: For handling asynchronous tasks such as sending notifications or processing payments.
Redis: Used for caching and session management.
Docker: Containerization tool for consistent development and deployment environments.
CI/CD Pipelines: Automated pipelines for testing and deploying code change

## Database Design

Defines the structure and relationships between core entities:

### Users

`id`, `username`, `email`, `password_hash`, `is_host`  
A user can create listings and make bookings.

### Properties

`id`, `title`, `description`, `location`, `owner_id`  
Belongs to a user; has many bookings and reviews.

### Bookings

`id`, `property_id`, `user_id`, `check_in`, `check_out`  
Linked to one user and one property.

### Payments

`id`, `booking_id`, `amount`, `payment_date`, `status`  
Connected to a booking transaction.

### Reviews

`id`, `property_id`, `user_id`, `rating`, `comment`  
Tied to a property and submitted by a user.

## Feature Breakdown

### User Management  

Handles registration, login, and user profiles.

### Property Management  

Create, edit, delete, and view property listings.

### Booking System  

Book and manage stays with check-in/out dates.

### Payment Processing  

Secure transaction handling for bookings.

### Review System  

Users can rate and review properties after a stay.

### API & Optimization  

REST & GraphQL APIs, Redis caching, and DB indexing.

## API Security

### Key Measures

Authentication– Validates user identity.
Authorization– Controls access to endpoints.
Rate Limiting– Prevents abuse and spam.
Secure Payments– Uses third-party payment gateways.

Security is essential for protecting user data and maintaining platform integrity.

## CI/CD pipelines

### Overview

CI/CD automates testing and deployment, enabling reliable and fast delivery of updates.

### Tools Used

GitHub Actions– Automates build and test workflows.
Docker & Docker Compose– Ensures consistent environments
