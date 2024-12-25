# DePauwTransportation

<!-- 
DePauwTransporation
|--backend/
    |--db.js  # database connection and queries
    |--database_models/ # directory contains representations of database entities like bicycles, users, and rentals
        |--Bicycle.js
        |--
    |--routes/
        |--bicycles.js
|--database/
    |--migrations/ # contains SQL files for schema updates
        |--001_create_bicycles_table.sql
        |--
    |--seeds/ # contains data for testing and initializing the database
        |--bicycles_seed.sql
        |--
    |--queries/  # organizes reusable SQL queries
        |--bicycles/
            |--get_all_bicycles.sql
            |--get_bicycle_by_id.sql
            |--update_bicycle_status.sql
        |--
    |--schema.sql # full database schema
|--public/ # contains frontend assets
    |--css/
        |--
    |--js/
        |--
    |--images/
        |--
    |--index.html #main HTML file
|--server.js
|--package.json
|--may cai download package gi do nua
-->

# Workflow:
1. ***Frontend Workflow (User Interaction)***
- User visits the homepage (`index.html`)
2. ***Backend Workflow (Processing Requests and Interacting with the Database)***
- Frontend sends a request to the backend
    - Frontend JavaScript (e.g `app.js`, `rental.js`, `user.js`) makes API requests to the backend using HTTP.
- Backend server receives the request
    - The server (`server.js`) handles incoming API requests.
    - The server uses routes defined in `routes/` (e.g. `bicycles.js`) to direct the request to the appopriate handler.
- Authentication and User Management
    - When a user attempts to log in or register, the server calls user routes (`users.js`).
    - The server queries the database to verify the user's credentials using SQL queries stored in `queries/users/` (e.g. `get_user_by_email.sql`).
    - If the user is registered, the server creates a session or token for authentication.
- Backend interacts with the database
     - The backend queries the database using SQL queries stored in `queries/` to fetch, create, update or delete records.
- Database updates
    - The database schema is updated when necessary using *migrations* stored in `migrations/`.
    - Seeding data in `seeds/` can populate initial data, like adding bicycles to the database for the first time.
- Respond the Frontend
    - Once request is processed, the backend sends a response (e.g. rental confirmation, user details) back to the frontend.
    - The frontend updates the user inteface to show the results (e.g. "Rental Confirmed" "Login Failed", etc)
3. ***Database Workflow (Handling Data)***
- Database Schema Setup
    - Migrations (e.g `001_create_bicycles_table.sql`) create the necessary tables (`bicycles`, `users`, `rentals`) in the database for storing user data, bicycle data, and rental transactions.
    - The migrations are applied in sequence to ensure proper schema evolution.
- Database Querying
    - When the backend receives a request (e.g. a user wants to rent a bicycle), it queries the database using the SQL queries stored in the `queries/` directory.
    - The database models (e.g. `bicycles.js`, `user.js`, etc) represent the data structure and facilitate CRUD operations on the database tables.
- Rentals and Bicycle Availability
    - When a bicycle is rented, the system updates the `rentals` table with details about the rental transaction.
    - The bicycle status (e.g availabe or rented) is updated in the `bicycles` table.
- Seed Data
    - During initial setup or for testing, *seed files* in `seeds/` can populate the database with sample data (e.g bicycle types, user data).