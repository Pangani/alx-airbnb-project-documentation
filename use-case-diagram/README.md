## 🏡 Airbnb Clone Backend Documentation

This project documents the backend design and requirements for an **Airbnb Clone** application.  
It focuses on the **database schema**, **features & functionalities**, and **system interactions**, ensuring the system is scalable, secure, and easy to extend.  

---

### 📚 Features & Functionalities

The backend provides the core functionality required for a rental marketplace:

- **User Management** – Registration, login (JWT + OAuth), profile updates, and role-based access.  
- **Property Listings** – Hosts can create, edit, and delete property listings with details such as price, location, amenities, and availability.  
- **Search & Filtering** – Guests can search listings by location, price range, amenities, and number of guests.  
- **Booking Management** – Guests can create bookings, cancel them, and view booking statuses.  
- **Payments** – Integration with secure payment gateways for guest payments and host payouts.  
- **Reviews & Ratings** – Guests leave reviews; hosts can respond. Reviews are tied to bookings.  
- **Notifications** – Email and in-app notifications for bookings, cancellations, and payments.  
- **Admin Dashboard** – Admins can manage users, listings, bookings, and payments.  
- **Technical & Non-Functional Requirements** – REST API, database management, security, scalability, and testing.  

📌 See the diagram below for a visual map of features:  

![Features & Functionalities](./features-and-functionalities/features-and-functionalities.png)  

---

#### 🗄️ Database Schema Overview

The database schema models the **core entities and relationships** of the Airbnb Clone backend, normalized to **Third Normal Form (3NF)** for efficiency and integrity.  

#### Key Entities
- **User** – Guests, hosts, and admins.  
- **Property** – Listings created by hosts.  
- **Booking** – Reservations linking guests to properties.  
- **Payment** – Linked to bookings, with secure methods.  
- **Review** – Ratings and comments tied to bookings.  
- **Message** – Direct communication between users.  
- **PaymentMethod** – Lookup table for valid payment types.  

#### Highlights
- **Normalization** – Prevents redundancy (e.g., centralized payment methods).  
- **Constraints** – Enforce valid data (unique emails, rating limits, valid booking statuses).  
- **Indexes** – Optimized performance for common queries (`email`, `property_id`, `booking_id`).  
- **Scalability** – Ready for extensions such as availability calendars or amenities.  

---

### 🎭 Use Case Diagram

The Use Case Diagram shows how different actors interact with the backend system.  

#### Actors
- **Guest** – Registers, books properties, makes payments, leaves reviews.  
- **Host** – Manages property listings, views bookings, responds to reviews, receives payouts.  
- **Admin** – Oversees users, listings, bookings, and payments through the admin dashboard.  
- **Payment Gateway** – Processes guest payments and host payouts.  

#### Purpose
This diagram helps visualize how core functionalities such as **registration, property management, booking, payments, reviews, and notifications** connect to system users and external services.  



