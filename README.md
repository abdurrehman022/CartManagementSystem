# Cart Management System

## Project Overview

The Cart Management System is a web application built using the MERN stack (MongoDB, Express.js, React, and Node.js). The purpose of this project is to provide a simple and efficient way to manage a shopping cart, allowing users to add, update, and remove products from their cart. The backend handles API requests and database operations, while the frontend provides a user-friendly interface for interacting with the cart.

## Project Structure

**Backend Directory Structure:**

```
/server
  /models
    Product.js
    Cart.js
  /routes
    productRoutes.js
    cartRoutes.js
  /middleware
    errorHandler.js
  app.js
  package.json
```

**Frontend Directory Structure:**

```
/client
  /src
    /components
    /context
    App.jsx
    main.jsx
  /public
  vite.config.js
  package.json
```

## Setup and Installation

### Backend Setup

1. **Clone the Repository:**
   ```
   git clone https://github.com/abdurrehman022/CartManagementSystem.git
   cd CartManagementSystem
   ```

2. **Install Backend Dependencies:**
   ```
   npm install
   ```

3. **Set Up Environment Variables:**
   - Create a `.env` file in the root directory and add the required variables.

4. **Start the Backend Server:**
   ```
   npm start
   ```

### Frontend Setup

1. **Navigate to the Client Directory:**
   ```
   cd client
   ```

2. **Install Frontend Dependencies:**
   ```
   npm install
   ```

3. **Set Up Environment Variables:**
   - Create a `.env` file in the client directory and add the required variables.

4. **Start the Frontend Development Server:**
   ```
   npm run dev
   ```

## API Endpoints

### Product Endpoints

- **GET /api/products**: Fetch all products.
  - **Response**: Array of product objects.

### Cart Endpoints

- **POST /api/cart**: Add or update a product in the cart.
  - **Request Body:**
    ```json
    {
      "userId": "exampleUserId",
      "productId": "exampleProductId",
      "quantity": 1
    }
    ```
  - **Response**: Updated cart object.

- **PUT /api/cart/:id**: Update the quantity of a product in the cart.
  - **Request Body:**
    ```json
    {
      "quantity": 2
    }
    ```
  - **Response**: Updated cart object.

- **DELETE /api/cart/:id**: Remove a product from the cart.
  - **Request Body:**
    ```json
    {
      "productId": "exampleProductId"
    }
    ```
  - **Response**: Updated cart object.

- **GET /api/cart**: Fetch the current state of the user's cart.
  - **Query Parameters:**
    - `userId`: The ID of the user.
  - **Response**: Cart object with total price.

## Testing

### Testing API Endpoints with Postman

1. **Install Postman:**
   - Download and install Postman from [here](https://www.postman.com/downloads).

2. **Import Collection:**
   - Import the provided Postman collection file (if available) or create a new collection.

3. **Set Environment Variables:**
   - Configure the environment variables in Postman for `MONGO_URI`, `VITE_API_URL`, and `PORT`.

4. **Test Endpoints:**
   - **GET /api/products**: Send a GET request to fetch all products.
   - **POST /api/cart**: Send a POST request to add a product to the cart.
   - **PUT /api/cart/:id**: Send a PUT request to update the quantity of a product in the cart.
   - **DELETE /api/cart/:id**: Send a DELETE request to remove a product from the cart.
   - **GET /api/cart**: Send a GET request to fetch the current state of the user's cart.

   Ensure that the backend server is running before testing the endpoints.

## Additional Information

Feel free to reach out if you have any questions or need further assistance.
