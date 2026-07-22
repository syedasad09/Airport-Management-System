# ✈️ Airport Management System (DBMS Project)

> A comprehensive Database Management System designed to streamline airport operations, flight scheduling, passenger bookings, baggage tracking, and resource allocation.

---

## 📌 Table of Contents
- [Overview](#-overview)
- [Key Features](#-key-features)
- [Database Schema & Architecture](#-database-schema--architecture)
  - [Core Entities](#core-entities)
  - [ER Diagram & Relations](#er-diagram--relations)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Database Setup](#database-setup)
- [Key SQL Operations & Stored Procedures](#-key-sql-operations--stored-procedures)
- [Future Roadmap](#-future-roadmap)
- [Contributing](#-contributing)
- [License & Contact](#-license--contact)

---

## 📖 Overview

The **Airport Management System** is a relational database project built to model and manage complex daily operations of a modern airport. It efficiently handles real-time flight schedules, passenger reservations, airline fleets, gate/terminal assignments, staff management, and security logs while maintaining database integrity and normalization.

---

## ✨ Key Features

* 🛫 **Flight Scheduling & Tracking:** Manage departure and arrival times, flight statuses (Scheduled, Delayed, In-Air, Landed), and routes.
* 🎫 **Passenger & Booking Management:** Handle passenger profiles, ticket reservations, seat allocations, and boarding pass generation.
* 🏢 **Airline & Aircraft Fleet Management:** Store and maintain data regarding participating airlines, aircraft models, capacities, and maintenance records.
* 🧳 **Baggage Tracking System:** Link baggage tags with passengers and flights for automated tracking and security handling.
* 🚪 **Gate & Terminal Allocation:** Manage gate assignments to prevent scheduling conflicts and optimize terminal traffic.
* 👥 **Staff & Crew Management:** Maintain records of pilots, cabin crew, ground staff, and security personnel assigned to specific flights or terminals.

---

## 🏗️ Database Schema & Architecture

### Core Entities
* **Airlines:** `Airline_ID`, `Name`, `IATA_Code`, `Country`
* **Aircraft:** `Aircraft_ID`, `Model`, `Capacity`, `Airline_ID`
* **Flights:** `Flight_Number`, `Origin`, `Destination`, `Departure_Time`, `Arrival_Time`, `Status`, `Gate_ID`, `Aircraft_ID`
* **Passengers:** `Passenger_ID`, `First_Name`, `Last_Name`, `Passport_Number`, `Email`, `Phone`
* **Bookings / Tickets:** `Ticket_Number`, `Passenger_ID`, `Flight_Number`, `Seat_Number`, `Class`, `Price`, `Booking_Date`
* **Baggage:** `Baggage_ID`, `Ticket_Number`, `Weight_KG`, `Status`
* **Gates & Terminals:** `Gate_ID`, `Terminal_Number`, `Gate_Number`, `Status`
* **Staff:** `Employee_ID`, `Name`, `Role`, `Assigned_Terminal`

### ER Diagram & Relations
```text
 +--------------+       1:N       +--------------+       1:N       +--------------+
 |   Airlines   | ───────────────> |   Aircraft   | ───────────────> |   Flights    |
 +--------------+                  +--------------+                  +--------------+
                                                                            │
                                                                 1:N        │ 1:N
                                                                            ▼
 +--------------+       1:N       +--------------+       1:N       +--------------+
 |  Passengers  | ───────────────> |   Bookings   | <─────────────── |    Gates     |
 +--------------+                  +--------------+                +--------------+
                                          │
                                     1:N  │
                                          ▼
                                   +--------------+
                                   |   Baggage    |
                                   +--------------+
