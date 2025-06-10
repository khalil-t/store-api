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
```

---

## 🔗 API Endpoints and Example URLs

| Description | Method | URL |
|------------|--------|-----|
| Get all products (static) | `GET` | `http://localhost:4000/api/v1/products/static` |
| Get all products (dynamic) | `GET` | `http://localhost:4000/api/v1/products` |
| Filter by name | `GET` | `http://localhost:4000/api/v1/products?name=chair` |
| Filter by company | `GET` | `http://localhost:4000/api/v1/products?company=ikea` |
| Filter by featured | `GET` | `http://localhost:4000/api/v1/products?featured=true` |
| Sort by price | `GET` | `http://localhost:4000/api/v1/products?sort=price` |
| Sort by price descending | `GET` | `http://localhost:4000/api/v1/products?sort=-price` |
| Select fields | `GET` | `http://localhost:4000/api/v1/products?fields=name,price` |
| Numeric filter (price > 30) | `GET` | `http://localhost:4000/api/v1/products?numericFilters=price>30` |
| Numeric filter (rating >= 4.5) | `GET` | `http://localhost:4000/api/v1/products?numericFilters=rating>=4.5` |
| Combine filters | `GET` | `http://localhost:4000/api/v1/products?company=ikea&numericFilters=price>=30,rating>4&sort=price` |

---

## 🧪 Testing the API

You can test these routes using:

- Postman
- Browser (for simple GET requests)
- cURL or any HTTP client

---

## 🛠️ Run the Project

```bash
npm install
npm run dev
```

Make sure MongoDB is running on your system.

---

## 🧑‍💻 Author

Built with ❤️ using Node.js and Express

