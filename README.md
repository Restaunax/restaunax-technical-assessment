# Restaunax Full-Stack Developer Technical Assessment

Welcome to the Restaunax Technical Assessment! 🍕🚀

Thank you for your interest in joining our team at Restaunax. This assessment is designed to evaluate your full-stack development skills within the context of our restaurant management platform. We're interested in seeing how you approach problems, structure your code, and create solutions that address real-world scenarios in the restaurant technology space.

## The Scenario

As a developer at Restaunax, one of your tasks is to develop a critical component of our restaurant management system: a **Real-time Order Management Dashboard**. Restaurant owners need a simple yet effective way to monitor incoming orders, update their status, and manage their kitchen operations efficiently.

## Your Task

You are free to use any backend language or framework, though we recommend using technologies aligned with our stack (Node.js/Express, PostgreSQL, Prisma). For the frontend, you **must use React with Material UI**.

### 1. Backend

Build a RESTful API with the following endpoints:

- `GET /orders` — List all orders with pagination and filtering
- `GET /orders/:id` — Retrieve a specific order with details
- `PATCH /orders/:id` — Update order status and preparation notes
- `POST /orders` — Create a new order (primarily for testing purposes)

Each order should include:

| Field            | Type                                                                             |
| ---------------- | -------------------------------------------------------------------------------- |
| id               | string or int                                                                    |
| customerName     | string                                                                           |
| customerEmail    | string                                                                           |
| orderType        | "delivery" \| "pickup"                                                           |
| items            | array of order items                                                             |
| status           | "pending" \| "confirmed" \| "preparing" \| "ready" \| "delivered" \| "completed" |
| total            | number                                                                           |
| createdAt        | ISO string                                                                       |
| scheduledFor     | ISO string (optional)                                                            |
| preparationNotes | string                                                                           |

Each order item should include:

| Field               | Type              |
| ------------------- | ----------------- |
| id                  | string or int     |
| name                | string            |
| quantity            | number            |
| price               | number            |
| specialInstructions | string (optional) |

### 2. Frontend

Create a responsive UI using **React and Material UI components** that includes:

- Dashboard overview showing orders by status
- Order detail view to see and update order information
- Filter/search functionality (by status, customer name, order type)
- Status management with drag-and-drop or dropdown functionality
- Responsive design that works on both desktop and mobile viewports

### 3. Data Seeding (Required)

- **Create a seed script** that generates and inserts a substantial set of mock order data (at least 30-50 orders) with various statuses, order types, and creation dates
- The script should be well-documented and easy to run
- Include a variety of scenarios (orders with multiple items, special instructions, scheduled orders, etc.)
- This seed data will be essential for testing your API endpoints and frontend functionality

## What We're Looking For

| Area              | What We Value                                            |
| ----------------- | -------------------------------------------------------- |
| Architecture      | Clean separation of concerns, scalable design            |
| Code Quality      | Readable, maintainable, and well-structured code         |
| UI Implementation | Proper use of Material UI components and design patterns |
| User Experience   | Intuitive, responsive interface for restaurant staff     |
| Testing           | Appropriate test coverage (unit/integration tests)       |
| Error Handling    | Robust handling of edge cases and failures               |
| Database Design   | Efficient schema and query patterns                      |
| Documentation     | Clear documentation and code comments                    |

## Seed Data (Example)

Here's a sample order you can use for reference:

```json
{
  "id": "ord_123456",
  "customerName": "Alex Johnson",
  "customerEmail": "alex@example.com",
  "orderType": "delivery",
  "status": "pending",
  "total": 42.5,
  "createdAt": "2024-05-07T18:30:00Z",
  "scheduledFor": "2024-05-07T19:15:00Z",
  "preparationNotes": "",
  "items": [
    {
      "id": "item_1",
      "name": "Margherita Pizza",
      "quantity": 2,
      "price": 15.99,
      "specialInstructions": "Extra cheese please"
    },
    {
      "id": "item_2",
      "name": "Caesar Salad",
      "quantity": 1,
      "price": 8.99,
      "specialInstructions": ""
    },
    {
      "id": "item_3",
      "name": "Garlic Bread",
      "quantity": 1,
      "price": 4.99,
      "specialInstructions": ""
    }
  ]
}
```

## Submission

Create your own GitHub repository for this project and send us the link (public or private with access). Include a detailed README that covers:

1. How to set up and run your application
2. Your technical choices and reasoning
3. Architecture overview (a diagram would be helpful)
4. What you'd improve or add with more time
5. Any challenges you faced and how you addressed them

## Questions?

If you have any questions about the assessment, please reach out to us directly. We're looking forward to seeing your solution!

Happy coding! 🧑‍💻
