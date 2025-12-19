# Task: Full-Stack Billing Application

## Overview
"XYZ Inc." is an online retailer. We need a **Billing Application** that allows users to submit orders via a web interface and process them through multiple payment gateways. The task is designed to evaluate full-stack skills, code quality, and architectural thinking.

## Order Payload
Each order contains:
- **Order number** (string)
- **User ID** (string)
- **Payable amount** (decimal)
- **Payment gateway ID** (string) – to map to the correct payment provider
- **Optional description** (string)

## Backend API Behavior
1. Receive an order via REST API.
2. Forward the order to the appropriate **mocked** payment gateway.
3. If payment succeeds, return a **receipt** including order number, amount, timestamp, and payment confirmation.
4. If payment fails, return a clear error response.
5. Ensure that processing the same order twice does not result in double payment.
6. Design your solution to support **multiple payment gateways** using extensible architecture (e.g., interfaces, dependency injection).

## Frontend Requirements
- Minimal web UI to:
  - Submit new orders
  - Display receipts or error messages
- **Preferred frameworks:** React or Angular, but other frameworks or plain JS are allowed.
- UI **polish is not evaluated**; focus on functional integration with the backend.

## Technical Requirements
- **Backend:** C# (.NET Core recommended)
- **Frontend:** React or Angular preferred
- Use **REST API principles**
- Cover backend logic with **unit tests**
- Code should follow **clean code and maintainable architecture principles**

## Run Instructions
- Provide clear steps to **run both backend and frontend locally**.
- Backend should start with a **single command** (`dotnet run`) or via Docker.
- Frontend should start with a **single command** (`npm install && npm start`) or via Docker.
- Any **configuration or environment variables** must be documented.
- The solution should work **out of the box** using mocked payment gateways—no external API keys or complex setup required.

## Optional Enhancements (Bonus Points)
- Logging and structured error handling
- API documentation (e.g., Swagger/OpenAPI)
- Retry logic for failed payments
- Integration tests or webhook notifications
- Basic frontend validation (e.g., required fields, number formatting)
- **Docker Compose setup** to run backend and frontend together

## Submission Guidelines
- Provide a GitHub repository link with your solution
- Include **detailed instructions to run the solution easily**
- The task should be completable in **3–5 hours**; focus on correctness, code quality, and architecture, not UI polish

## Evaluation Checklist
1. Backend API accepts orders and returns receipt/error
2. Payment gateways are mocked and handled correctly
3. Idempotency is respected (no double payments for the same order)
4. UI submits orders and displays results
5. Backend logic is covered with unit tests
6. Code is clean, maintainable, and structured for extensibility
7. Optional: logging, Swagger, retries, integration tests, Docker Compose
