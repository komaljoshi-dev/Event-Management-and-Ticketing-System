# Event-Management-ticketing-system
Assignment 1 for backend development and mern integration

## Description

This project implements a MongoDB-based Event Management and Ticketing System. It manages users, events, ticket bookings, and categories using multiple collections. CRUD operations, aggregation pipelines, and indexes are used to efficiently store, retrieve, and analyze data.

Database Name - eventManagementDB

## Collections Used

- Users – Stores event organizers and attendees
- Events – Stores event details created by organizers
- Tickets – Stores ticket booking and cancellation information
- Categories – Stores event categories such as Music, Tech, Sports, etc.

## Schema Structure and Relationships

The database follows a relational structure using references between collections:

- The Users collection stores both organizers and attendees. The role field differentiates whether a user can create events or book tickets.
- The Events collection references the organizer through organizerId, which corresponds to userId in the Users collection. Each event is created by exactly  one organizer.
- The Tickets collection references both ```eventId``` (from Events) and ```userId``` (from Users), allowing attendees to book multiple tickets for an event.
- The Categories collection is used to classify events. Each event stores a category value, enabling grouping and filtering of events by category.

This structure enables efficient event management, ticket tracking, and aggregation-based reporting.

## Key Features

- CRUD operations on all collections
- Ticket booking and cancellation handling
- Aggregation pipelines for reporting
- Indexes for performance optimization
- Sample data with at least 20 documents per collection
- Aggregation Reports Implemented

1. Top 5 events by ticket sales
2. Total revenue earned by an organizer
3. Number of attendees per event
4. Events grouped by category and status

## Indexes

Indexes are created on frequently searched fields:

- category
- dateTime
These indexes improve performance for event searches and reporting queries.

## Assumptions

- Ticket revenue is calculated as price × quantity and is stored in totalAmount
- Only booked tickets are considered in revenue and attendance calculations
- Each event is created by one organizer
- A user can book multiple tickets for an event

## How to Run

Open MongoDB shell or MongoDB Compass
Use the database:
```use eventManagementDB```
Run the insert, CRUD, aggregation, and index queries provided in the PDF

Author
Komal Joshi
