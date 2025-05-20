# Restaunax Full-Stack Developer Technical Assessment

Welcome to the Restaunax Technical Assessment! 🍕🚀

Thank you for your interest in joining our team at Restaunax. This assessment is designed to evaluate your essential full-stack development skills within the context of our restaurant management platform.

## The Scenario

As a developer at Restaunax, you'll be working on our restaurant management system. Your task is to create a simplified version of a **Real-time Order Management Dashboard** that allows restaurant owners to view and update orders.

## Your Task

Implement a basic version of the order management system using Node.js/Express and React with Material UI.

### 1. Backend

Build a simple API with the following endpoints:

- `GET /orders` — List all orders (simple filtering by status optional)
- `GET /orders/:id` — Retrieve a specific order
- `PATCH /orders/:id` — Update order status
- `POST /orders` — Create a new order (for testing)

Each order should include:

| Field        | Type                                               |
| ------------ | -------------------------------------------------- |
| id           | string or int                                      |
| customerName | string                                             |
| orderType    | "delivery" \| "pickup"                             |
| items        | array of order items                               |
| status       | "pending" \| "preparing" \| "ready" \| "delivered" |
| total        | number                                             |
| createdAt    | ISO string                                         |

Each order item should include:

| Field    | Type          |
| -------- | ------------- |
| id       | string or int |
| name     | string        |
| quantity | number        |
| price    | number        |

### 2. Frontend

Create a simple UI using **React and Material UI components** that includes:

- Dashboard showing orders by status
- Basic order details view
- Ability to update order status
- Mobile-responsive design

### 3. Data Storage

You may use:

- PostgreSQL with Prisma (preferred)
- SQLite
- JSON file (simplest option)
- In-memory data structure (for the quickest implementation)

### 4. Data Seeding

- Create a simple seed script that generates 10-15 mock orders
- Include a variety of statuses and order types

## What We're Looking For

| Area              | What We Value                                      |
| ----------------- | -------------------------------------------------- |
| Architecture      | Clean, organized code structure                    |
| UI Implementation | Proper use of Material UI components               |
| User Experience   | Functional, responsive interface                   |
| API Integration   | Successful connection between frontend and backend |
| Error Handling    | Basic handling of common errors                    |

## Bonus Points

Feel free to showcase your skills by implementing additional features beyond the basic requirements. Some ideas include:

- Containerizing your application with Docker
- Adding data visualization (charts/graphs showing order statistics)
- Implementing real-time updates with WebSockets
- Adding authentication/authorization
- Creating a more advanced filtering system
- Implementing any creative feature that enhances the restaurant management experience

These extras are not required but can help demonstrate your capabilities and creativity.

## Seed Data (Example)

Here's a sample order you can use for reference:

```json
{
  "id": "ord_123456",
  "customerName": "Alex Johnson",
  "orderType": "delivery",
  "status": "pending",
  "total": 42.5,
  "createdAt": "2024-05-07T18:30:00Z",
  "items": [
    {
      "id": "item_1",
      "name": "Margherita Pizza",
      "quantity": 2,
      "price": 15.99
    },
    {
      "id": "item_2",
      "name": "Caesar Salad",
      "quantity": 1,
      "price": 8.99
    }
  ]
}
```

## Submission

Create a GitHub repository for this project and send us the link. Include a basic README that covers:

1. How to set up and run your application
2. Brief overview of your implementation
3. Any challenges you faced

## Submission Timeline

You will have at least 7 days from receiving this assessment to complete and submit your solution. Focus on implementing the core functionality rather than perfecting every detail.

Happy coding! 🧑‍💻
