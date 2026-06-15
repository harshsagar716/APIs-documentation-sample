# APIs-documentation-sample
APIs Documentation for the startup project "Wansafar"
# Tour & Adventure Booking — API Documentation

> **OpenAPI 3.0 / Swagger documentation** for a Tour, Safari & Adventure booking platform.  
> Created during my role as **Associate Product Manager at Orgosys Private Limited** (Oct 2025 – Mar 2026).

---

## About This Project

This repository contains the API documentation I authored and maintained for a live travel-tech startup building a **tour, safari, and adventure booking platform**.

As the APM, I was responsible for:
- Defining and documenting **API endpoint specifications** (GET, POST, PUT, DELETE)
- Conducting **backend QA** and testing all endpoints via **Postman**
- Optimizing server response times — achieving **sub-10ms latency** on key endpoints
- Maintaining live **third-party integrations** (e.g., TripAdvisor API)
- Translating complex backend logic into **clear, usable documentation** for the dev team

> **Note:** This repo uses **generic/sample data** to protect the company's proprietary codebase. The structure, endpoint logic, and documentation style reflect the actual work done.

---

## What's Inside

```
api-documentation-sample/
│
├── swagger.yaml          # Full OpenAPI 3.0 spec — Tours, Bookings, Customers
└── README.md             # This file
```

---

## API Modules Documented

### 1. Tours
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/tours` | Fetch all available tours with filters (category, location, price) |
| GET | `/tours/{tourId}` | Get full details of a specific tour |

### 2. Bookings
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/bookings` | Fetch all bookings (filterable by status, customer) |
| POST | `/bookings` | Create a new booking independently of parent tour |
| GET | `/bookings/{bookingId}` | Fetch a specific booking |
| PUT | `/bookings/{bookingId}` | Update booking details (date, participants, status) |
| DELETE | `/bookings/{bookingId}` | Cancel and remove a booking |

### 3. Customers
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/customers` | Register a new customer |
| GET | `/customers/{customerId}` | Fetch customer profile |
| PUT | `/customers/{customerId}` | Update customer details |
| DELETE | `/customers/{customerId}` | Delete a customer record |

---

## Tools Used

| Tool | Purpose |
|------|---------|
| **Swagger / OpenAPI 3.0** | API documentation standard |
| **Postman** | Endpoint testing & latency benchmarking |
| **AI-assisted scripting** | Formula optimization and backend QA automation |

---

## How to View This Documentation

You can render this Swagger file visually in 2 ways:

**Option 1 — Swagger Editor (Online, no install needed):**
1. Go to [editor.swagger.io](https://editor.swagger.io)
2. Delete the default content
3. Copy-paste the contents of `swagger.yaml`
4. The interactive docs render on the right side instantly

**Option 2 — VS Code:**
1. Install the **OpenAPI (Swagger) Editor** extension
2. Open `swagger.yaml`
3. Press `Ctrl+Shift+P` → "Preview Swagger"

---

## Key Technical Insight

One of the more complex things I documented was the logic allowing **individual bookings to be updated independently of their parent tour record**. This was a non-obvious backend design that required careful endpoint structuring — specifically the `PUT /bookings/{bookingId}` endpoint — to ensure partial updates didn't cascade unintentionally to other bookings under the same tour.

---

## About Me

**Harsh Sagar** — Associate Product Manager | MBA Graduate  
sagarharsh716@gmail.com  
[LinkedIn](https://www.linkedin.com/in/harshsagar9318)

---

*This documentation sample is shared for portfolio purposes. All company-specific data has been replaced with generic examples.*
