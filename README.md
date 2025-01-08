# Inventory Management System

An Inventory Management System built using **Node.js**, **Express.js**, and **MongoDB** for backend functionality. This system supports basic CRUD operations for managing inventory items.

## Features

- Add new products.
- Retrieve all products.
- Update existing product details.
- Delete products.
- MongoDB integration for persistent storage.
- Deployed on **Vercel** for easy access.

---

## Tech Stack

- **Node.js**: Backend runtime.
- **Express.js**: Web framework for building APIs.
- **MongoDB**: NoSQL database for persistent storage.
- **Mongoose**: ODM for MongoDB.
- **Vercel**: Deployment platform.

---

## API Endpoints

Base URL: [https://inventory-management-ov6oi98cu-shivarths-projects.vercel.app](https://inventory-management-ov6oi98cu-shivarths-projects.vercel.app)

### **1. Add a Product**
- **POST** `/api/products`
- **Request Body** (JSON):
  ```json
  {
    "name": "Laptop",
    "quantity": 50,
    "price": 999.99
  }
  ```
- **Response**:
  ```json
  {
    "_id": "6760188851e128afca774358",
    "name": "Laptop",
    "quantity": 50,
    "price": 999.99,
    "createdAt": "2024-12-16T10:20:00.000Z",
    "updatedAt": "2024-12-16T10:20:00.000Z",
    "__v": 0
  }
  ```

### **2. Get All Products**
- **GET** `/api/products`
- **Response**:
  ```json
  [
    {
      "_id": "6760188851e128afca774358",
      "name": "Laptop",
      "quantity": 50,
      "price": 999.99,
      "createdAt": "2024-12-16T10:20:00.000Z",
      "updatedAt": "2024-12-16T10:20:00.000Z",
      "__v": 0
    }
  ]
  ```

### **3. Update a Product**
- **PUT** `/api/products/:id`
- Replace `:id` with the product ID.
- **Request Body** (JSON):
  ```json
  {
    "name": "Updated Laptop",
    "quantity": 30,
    "price": 1099.99
  }
  ```
- **Response**:
  ```json
  {
    "_id": "6760188851e128afca774358",
    "name": "Updated Laptop",
    "quantity": 30,
    "price": 1099.99,
    "createdAt": "2024-12-16T10:20:00.000Z",
    "updatedAt": "2024-12-16T12:00:00.000Z",
    "__v": 0
  }
  ```

### **4. Delete a Product**
- **DELETE** `/api/products/:id`
- Replace `:id` with the product ID.
- **Response**:
  ```
  Status: 204 No Content
  ```

---

## How to Run Locally

### Prerequisites
- Install [Node.js](https://nodejs.org/).
- Install [MongoDB](https://www.mongodb.com/atlas/database).

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/inventory-management.git
   cd inventory-management
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the project root and add your environment variables:
   ```
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   NODE_ENV=development
   ```

4. Start the server:
   ```bash
   node app.js
   ```

5. Access the API at `http://localhost:5000`.

---

## Deployment

The project is deployed on Vercel:  
**Base URL**: [https://inventory-management-ov6oi98cu-shivarths-projects.vercel.app](https://inventory-management-ov6oi98cu-shivarths-projects.vercel.app)
**Output** : ![image](https://github.com/user-attachments/assets/cd5a829c-9137-4925-8927-3bcfe75ced6c)

---

## Project Structure

```
inventory-management/
├── controllers/
│   └── productController.js    # Controller logic for CRUD operations
├── models/
│   └── Product.js              # Mongoose schema for Product
├── routes/
│   └── productRoutes.js        # API routes
├── app.js                      # Entry point
├── .env                        # Environment variables
├── package.json                # Dependencies and scripts
└── README.md                   # Project documentation
```

---

## Future Enhancements

- Add user authentication and authorization.
- Implement frontend for better UI/UX.
- Add pagination and search functionality for product listing.
- Set up unit and integration tests.

---

## Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Submit a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

### **Steps to Use This README**
1. Copy the content into a `README.md` file at the root of your project directory.
2. Replace placeholder URLs, such as `<your-username>`, with your actual GitHub username or project details.
3. Push the changes to GitHub:
   ```bash
   git add README.md
   git commit -m "Add README"
   git push origin main
