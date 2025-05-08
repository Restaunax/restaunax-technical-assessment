Restaunax Full-Stack Developer Technical Assessment
Welcome to the Restaunax Technical Assessment! 🍕🚀
Thank you for your interest in joining our team at Restaunax. This assessment is designed to evaluate your full-stack development skills within the context of our restaurant management platform. We're interested in seeing how you approach problems, structure your code, and create solutions that address real-world scenarios in the restaurant technology space.
📘 The Scenario
As a developer at Restaunax, one of your tasks is to develop a critical component of our restaurant management system: a Real-time Order Management Dashboard. Restaurant owners need a simple yet effective way to monitor incoming orders, update their status, and manage their kitchen operations efficiently.
📋 Your Task
You are free to use any backend language or framework, though we recommend using technologies aligned with our stack (Node.js/Express, PostgreSQL, Prisma). For the frontend, you must use React with Material UI.

1. Backend
   Build a RESTful API with the following endpoints:

GET /orders — List all orders with pagination and filtering
GET /orders/:id — Retrieve a specific order with details
PATCH /orders/:id — Update order status and preparation notes
POST /orders — Create a new order (primarily for testing purposes)

Each order should include:
FieldTypeidstring or intcustomerNamestringcustomerEmailstringorderType"delivery" | "pickup"itemsarray of order itemsstatus"pending" | "confirmed" | "preparing" | "ready" | "delivered" | "completed"totalnumbercreatedAtISO stringscheduledForISO string (optional)preparationNotesstring
Each order item should include:
FieldTypeidstring or intnamestringquantitynumberpricenumberspecialInstructionsstring (optional) 2. Frontend
Create a responsive UI using React and Material UI components that includes:

Dashboard overview showing orders by status
Order detail view to see and update order information
Filter/search functionality (by status, customer name, order type)
Status management with drag-and-drop or dropdown functionality
Responsive design that works on both desktop and mobile viewports
Bonus: Implement real-time updates using Socket.io

3. Real-time Features (Highly Recommended)

Implement WebSocket connection (Socket.io preferred) for real-time order updates
New orders should appear in the dashboard without refreshing
Status updates should be reflected in real-time across connected clients

4. Data Seeding (Required)

Create a seed script that generates and inserts a substantial set of mock order data (at least 30-50 orders) with various statuses, order types, and creation dates
The script should be well-documented and easy to run
Include a variety of scenarios (orders with multiple items, special instructions, scheduled orders, etc.)
This seed data will be essential for testing your API endpoints and frontend functionality

✅ What We're Looking For
AreaWhat We ValueArchitectureClean separation of concerns, scalable designCode QualityReadable, maintainable, and well-structured codeReal-time ImplementationEffective use of WebSockets for live updatesUI ImplementationProper use of Material UI components and design patternsUser ExperienceIntuitive, responsive interface for restaurant staffTestingAppropriate test coverage (unit/integration tests)Error HandlingRobust handling of edge cases and failuresDatabase DesignEfficient schema and query patternsDocumentationClear documentation and code comments
🧪 Seed Data (Example)
Here's a sample order you can use for reference:
json{
"id": "ord_123456",
"customerName": "Alex Johnson",
"customerEmail": "alex@example.com",
"orderType": "delivery",
"status": "pending",
"total": 42.50,
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
🚀 Running the Application
Please provide detailed instructions for setting up and running your application. Your README should include step-by-step instructions similar to the following:
Backend Setup
bash# Clone the repository
git clone https://github.com/yourusername/restaunax-assessment.git
cd restaunax-assessment

# Install backend dependencies

cd backend
npm install

# Set up your environment variables

cp .env.example .env

# Edit .env file with your database credentials

# Setup database and run migrations

npx prisma migrate dev

# Run the seed script to populate database with mock orders

npm run seed

# or directly: node scripts/seed.js

# Start the backend server

npm run dev

# Server should be running on http://localhost:3000

Frontend Setup
bash# In a new terminal, navigate to the frontend directory
cd ../frontend

# Install frontend dependencies

npm install

# Start the frontend development server

npm run dev

# Frontend should be accessible at http://localhost:5173

⌛ Time Expectations
We expect this assessment to take approximately 4-6 hours. Don't worry about implementing every feature perfectly—focus on demonstrating your technical approach and code quality.
📮 Submission
Please send us a link to your GitHub repository (public or private with access). Include a README that covers:

How to set up and run your application
Your technical choices and reasoning
Architecture overview (a diagram would be helpful)
What you'd improve or add with more time
Any challenges you faced and how you addressed them

Questions?
If you have any questions about the assessment, please reach out to us directly. We're looking forward to seeing your solution!
Happy coding! 🧑‍💻
