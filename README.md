Capstone: Restaurant Reservation System
#Link to the deployed APP: [Restaurant Reservation APP] (https://resto-joy.herokuapp.com/dashboard)

App story
You have been hired as a full stack developer at Periodic Tables, a startup that is creating a reservation system for fine dining restaurants. The software is used only by restaurant personnel when a customer calls to request a reservation. At this point, the customers will not access the system online.

Database setup
Set up four new ElephantSQL database instances - development, test, preview, and production - by following the instructions in the "PostgreSQL: Creating & Deleting Databases" checkpoint.
After setting up your database instances, connect DBeaver to your new database instances by following the instructions in the "PostgreSQL: Installing DBeaver" checkpoint.
Knex
Run npx knex commands from within the back-end folder, which is where the knexfile.js file is located.

Installation
Fork and clone this repository.
Run cp ./back-end/.env.sample ./back-end/.env.
Update the ./back-end/.env file with the connection URL's to your ElephantSQL database instance.
Run cp ./front-end/.env.sample ./front-end/.env.
You should not need to make changes to the ./front-end/.env file unless you want to connect to a backend at a location other than http://localhost:5000.
Run npm install to install project dependencies.
Run npm run start:dev to start your server in development mode.
If you have trouble getting the server to run, reach out for assistance.

Running tests
This project has unit, integration, and end-to-end (e2e) tests. You have seen unit and integration tests in previous projects. End-to-end tests use browser automation to interact with the application just like the user does. Once the tests are passing for a given user story, you have implemented the necessary functionality.

Test are split up by user story. You can run the tests for a given user story by running:

npm run test:X where X is the user story number.

Have a look at the following examples:

npm run test:1 runs all the tests for user story 1 (both frontend and backend).
npm run test:3:backend runs only the backend tests for user story 3.
npm run test:3:frontend runs only the frontend tests for user story 3.
Create and list reservations
As a restaurant manager
I want to create a new reservation when a customer calls
so that I know how many customers will arrive at the restaurant on a given day. I only want to allow reservations to be created on a day when we are open
so that users do not accidentally create a reservation for days when we are closed.
I only want to allow reservations to be created during business hours, up to 60 minutes before closing
so that users do not accidentally create a reservation for a time we cannot accommodate.

Screenshots
Create Reservation

Seat reservation
As a restaurant manager,
When a customer with an existing reservation arrives at the restaurant
I want to seat (assign) their reservation to a specific table
so that I know which tables are occupied and free.

Screenshots
Seat Reservation

US-05 Finish an occupied table
As a restaurant manager
I want to free up an occupied table when the guests leave
so that I can seat new guests at that table.

Screenshots
Finish Occupied tables

US-06 Reservation Status
As a restaurant manager
I want a reservation to have a status of either booked, seated, or finished
so that I can see which reservation parties are seated, and finished reservations are hidden from the dashboard.

Screenshots
Reservation status

US-07 Search for a reservation by phone number
As a restaurant manager
I want to search for a reservation by phone number (partial or complete)
so that I can quickly access a customer's reservation when they call about their reservation.

Screenshots
Reservation search

US-08 Change an existing reservation
As a restaurant manager
I want to be able to modify a reservation if a customer calls to change or cancel their reservation
so that reservations are accurate and current.

Screenshots
Reservation status

API
There are two datasets that are a part of this project: reservations and tables.

You can view all the data inside of the Restaurant-reservation-app\back-end\src\db\data\seeds folder. Each data set can be accessed via a named property in this file. The following is a partial listing of the data in data/db.json:

reservation: { "first_name": "Rick", "last_name": "Sanchez", "mobile_number": "202-555-0164", "reservation_date": "2020-12-31", "reservation_time": "20:00:00", "people": 6, "created_at": "2020-12-10T08:30:32.326Z", "updated_at": "2020-12-10T08:30:32.326Z" },

Table : { table_name: "Bar #1", capacity: 1 },
