# Product API Documentation

This is a simple Express API for managing products with features like filtering, sorting, and selecting specific fields. The backend connects to a MongoDB database and uses Mongoose to interact with the `Task` model for product data.

---

## 🚀 Features

- **Get All Products (Static):** Retrieve all products sorted by price.
- **Get All Products (Dynamic):** Retrieve products with dynamic filtering, sorting, and field selection based on query parameters.
- **Numeric Filtering:** Filter products by numeric fields like `price` and `rating` with operators (`>`, `<`, `>=`, `<=`, `=`).
- **Sorting:** Sort products by one or more fields.
- **Field Selection:** Select specific fields to return (e.g., only `name`, `price`, etc.).

---

## 📦 Requirements

- Node.js
- Express
- Mongoose (for MongoDB interaction)

---

## 📂 Folder Structure

```txt
your-project/
├── db/
│   └── connect.js          # MongoDB connection logic
├── middleware/
│   └── error-handler.js    # Error handling middleware
│   └── not-found.js        # 404 not found middleware
├── models/
│   └── Task.js             # Mongoose model for products
├── routes/
│   └── products.js         # Routes for handling product-related requests
├── server.js               # Main server file
├── package.json            # Project dependencies and scripts
└── README.md               # Project documentation
