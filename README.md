# 🛒 Assignment 2 – E-Commerce Product API

## 📌 Objective

Build a REST API using **Express.js** that manages product data using an **in-memory JSON array**.

This API allows you to:
- View products
- Add new products
- Update product details

> No database is used.

---

## 🧾 Product Structure

Each product looks like this:

```json
{ "id": 1, "name": "Wireless Mouse", "category": "Electronics", "price": 799, "stock": 25, "rating": 4.3 }
```

---

## 📦 Sample Data

```js
const products = [
  { id: 1, name: "Wireless Mouse", category: "Electronics", price: 799, stock: 25, rating: 4.3 },
  { id: 2, name: "Running Shoes", category: "Footwear", price: 2499, stock: 40, rating: 4.5 },
  { id: 3, name: "Laptop Stand", category: "Accessories", price: 999, stock: 30, rating: 4.2 },
  { id: 4, name: "Smart Watch", category: "Electronics", price: 4999, stock: 12, rating: 4.4 },
  { id: 5, name: "Backpack", category: "Fashion", price: 1599, stock: 50, rating: 4.1 }
];
```

---

## 🚀 Technologies Used

- **Node.js**
- **Express.js**
- **CORS Middleware**
- **In-Memory JSON Array**

---

## ▶️ How to Run Locally

1. **Clone Repository**
   ```bash
   git clone https://github.com/jalpatel2646/Node_ass-2.git
   ```

2. **Go to project folder**
   ```bash
   cd Node_ass-2
   ```

3. **Install dependencies**
   ```bash
   npm install
   ```

4. **Run server**
   ```bash
   node index.js
   ```

5. Server runs on: **http://localhost:3000**

---

## 📚 API Routes

### ✅ GET Routes

| Route | Description | Status |
|-------|-------------|--------|
| `GET /products` | Get All Products | 200 |
| `GET /products/:id` | Get Product by ID (e.g. `/products/3`) | 200 or 404 |
| `GET /products/category/:categoryName` | Get Products by Category (e.g. `/products/category/Electronics`) | 200 |

### ✅ POST Route

| Route | Description | Status |
|-------|-------------|--------|
| `POST /products` | Add New Product | 201 |

**Body Example:**
```json
{
  "name": "Bluetooth Speaker",
  "category": "Electronics",
  "price": 2999,
  "stock": 20,
  "rating": 4.6
}
```

### ✅ PUT Routes

| Route | Description | Status |
|-------|-------------|--------|
| `PUT /products/:id` | Replace Entire Product | 200 or 404 |
| `PUT /products/:id/stock` | Update Stock Only (`{ "stock": 60 }`) | 200 or 404 |
| `PUT /products/:id/price` | Update Price Only (`{ "price": 1299 }`) | 200 or 404 |

---

## 📊 Status Codes Used

| Code | Meaning |
|------|---------|
| 200 | Success |
| 201 | Created |
| 404 | Not Found |

---

## 🧪 Testing

Use **Postman** to test all routes.

📖 **API Documentation:** [View on Postman](https://documenter.getpostman.com/view/50839389/2sBXcGFfQe)