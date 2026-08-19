# 📚 Artisan's Corner - REST API Documentation

Detailed specification of backend REST API endpoints, request bodies, and authentication headers for **Artisan's Corner**.

---

## 🔐 Authentication Endpoints

### `POST /api/auth/register`
Create a new user account (Buyer or Seller).

**Request Body:**
```json
{
  "name": "Jane Artisan",
  "email": "jane@example.com",
  "password": "password123",
  "role": "seller"
}
```

### `POST /api/auth/login`
Authenticate existing user and return JWT bearer token.

**Response:**
```json
{
  "_id": "60d5ecb8b5c9c22b9c8b4567",
  "name": "Jane Artisan",
  "email": "jane@example.com",
  "role": "seller",
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
}
```

---

## 🛍️ Product Endpoints

### `GET /api/products`
Fetch catalog products with search, category filtering, and pagination.

### `GET /api/products/:id`
Get single product details with vendor info and customer reviews.

### `POST /api/products` *(Protected: Seller)*
Create a new handcrafted product listing.

---

## 🛒 Order & Checkout Endpoints

### `POST /api/orders` *(Protected: Buyer)*
Place a new customer order with cart items and shipping details.

### `GET /api/orders/myorders` *(Protected: Buyer)*
Fetch order history for logged-in buyer.

### `PUT /api/orders/:id/status` *(Protected: Seller / Admin)*
Update order lifecycle state (`Processing` -> `Shipped` -> `Delivered`).

---

## 📊 Admin & Analytics Endpoints

### `GET /api/admin/stats` *(Protected: Admin)*
Fetch platform-wide GMV, vendor store metrics, and commission metrics.

---

*Document Date: August 19, 2026*
