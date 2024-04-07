# Used Cars Pricing API

This is a REST API built with Node.js and TypeScript using:

- NestJS
- TypeORM
- SQLite

That application allows managing used cars prices. Users can submit reports about sold cars, and the application can calculate the estimate based on the average price of the car from the submitted reports.

## How to Run the Application

1. **Installing Dependencies**: Open an NPM (Node Package Manager) terminal and run:

npm install


2. **Creating a `.env.development` File**: Fill it with the following environment variables:
DB_NAME=db.sqlite
COOKIE_KEY=alskdfjlkj


3. **Database Migration**: Run the following command in your terminal: 

npm run typeorm migration:generate -- -n initial-schema -o


4. **Starting the App**: Simply type:
npm start


After a few seconds, the application will be up and running, and all functionality will be available.

## Endpoints to Use

| Route          | Method | Description            | Authentication  |
|----------------|--------|------------------------|-----------------|
| /auth/signup   | POST   | Register a new user    | No              |
| /auth/signin   | POST   | Login a user           | No              |
| /auth/signout  | POST   | Logout a user          | Yes             |
| /auth/profile  | GET    | Get the current user   | Yes             |
| /auth/:id      | GET    | Get other user profile | No              |
| /auth/:id      | PATCH  | Update profile info    | Yes             |
| /reports       | POST   | Create a new report    | Yes             |
| /reports/:id   | PATCH  | Approve report         | Yes (Admin only)|
| /reports       | GET    | Get the estimate       | No              |

Feel free to use these endpoints to interact with the API.
