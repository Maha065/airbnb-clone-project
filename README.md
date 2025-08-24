## Overview
This project is a simplified clone of **Airbnb**, built to practice and showcase full-stack web development skills.  
The goal is to replicate core features of Airbnb, such as browsing listings, viewing property details, user authentication, and booking functionality.

## Project Goals
- Build a responsive and user-friendly interface inspired by Airbnb.
- Implement authentication (sign up, login, logout).
- Allow users to create, view, and book property listings.
- Practice modern web development workflows and deployment.

## Technology Stack

### Frontend
- **React**: A JavaScript library for building dynamic and reusable user interfaces.  
- **Tailwind CSS**: A utility-first CSS framework for creating modern, responsive designs quickly.  
- **Axios**: A promise-based HTTP client for handling API requests between frontend and backend.  

### Backend
- **Node.js**: A JavaScript runtime environment for running server-side code.  
- **Express.js**: A lightweight web framework for Node.js, used to build RESTful APIs.  

### Database
- **MongoDB**: A NoSQL database for storing flexible and scalable data.  
- **Mongoose ORM**: An object data modeling (ODM) library for MongoDB to manage schema and queries.  

### Authentication
- **JWT (JSON Web Tokens)**: A secure method for user authentication and authorization.  

### Deployment
- **Vercel**: A hosting platform for frontend applications (React).  
- **Render/Heroku**: Cloud platforms for deploying backend services (Node.js + Express).  

---

## Database Design

### Entities and Fields

1. **Users**
   - `user_id`: Unique identifier  
   - `name`: Full name of the user  
   - `email`: Unique email address  
   - `password`: Hashed password for authentication  
   - `role`: Defines whether the user is a guest or a host  

2. **Properties**
   - `property_id`: Unique identifier  
   - `title`: Name of the property listing  
   - `description`: Details about the property  
   - `location`: Address or city  
   - `price_per_night`: Cost for one night stay  

3. **Bookings**
   - `booking_id`: Unique identifier  
   - `user_id`: Reference to the user who made the booking  
   - `property_id`: Reference to the booked property  
   - `check_in`: Start date of the booking  
   - `check_out`: End date of the booking  

4. **Reviews**
   - `review_id`: Unique identifier  
   - `user_id`: Reference to the user who wrote the review  
   - `property_id`: Reference to the reviewed property  
   - `rating`: Numerical score (e.g., 1–5)  
   - `comment`: Text feedback  

5. **Payments**
   - `payment_id`: Unique identifier  
   - `booking_id`: Reference to the related booking  
   - `amount`: Total payment amount  
   - `payment_method`: e.g., credit card, PayPal  
   - `status`: e.g., pending, completed, failed  

### Relationships
- A **User** can list multiple **Properties**.  
- A **User** can make multiple **Bookings**, but each **Booking** belongs to one **Property**.  
- A **Property** can have many **Reviews**, and each **Review** is written by a single **User**.  
- A **Booking** is linked to one **Payment**, but a **User** can have multiple **Payments** across different bookings.  

---

## Statu
