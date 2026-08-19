# 🗺️ Artisan's Corner - Complete Project Structure & Architecture

A detailed overview of the folder structure, components, context state providers, and backend models for **Artisan's Corner**.

---

## 📁 Repository Directory Hierarchy

```
artisans-corner/
├── client/                     # Frontend React Application (Vite + Tailwind CSS)
│   ├── public/                 # Static Assets & Product Images
│   │   ├── assets/             # High-resolution handcrafted product photos
│   │   └── index.html          # Public HTML Template
│   ├── src/
│   │   ├── components/         # Reusable Layout Components
│   │   │   ├── Navbar.jsx      # Navigation bar with search, cart badge & profile menu
│   │   │   └── Footer.jsx      # Site footer with brand info & links
│   │   ├── context/            # React Context API State Providers
│   │   │   ├── AuthContext.jsx # User Authentication & Role Token State
│   │   │   └── CartContext.jsx # Shopping Cart Items & LocalStorage persistence
│   │   ├── data/
│   │   │   └── catalogData.js  # Pre-seeded product catalog dataset
│   │   ├── pages/              # Application Page Views
│   │   │   ├── Home.jsx        # Landing page with hero banner & featured categories
│   │   │   ├── Products.jsx    # Catalog filter & search grid
│   │   │   ├── ProductDetails.jsx # Single product detail view
│   │   │   ├── Cart.jsx        # Shopping cart item management
│   │   │   ├── Checkout.jsx    # Shipping & Payment simulation checkout
│   │   │   ├── OrderDetails.jsx # Order status & tracking detail
│   │   │   ├── Profile.jsx     # Buyer profile & past orders
│   │   │   ├── BecomeSeller.jsx # Vendor onboarding form
│   │   │   ├── SellerDashboard.jsx # Vendor inventory & order processing dashboard
│   │   │   ├── AdminDashboard.jsx  # Admin analytics & platform moderation
│   │   │   ├── Login.jsx       # Login form with instant demo autofill buttons
│   │   │   ├── Register.jsx    # User registration form
│   │   │   └── NotFound.jsx    # 404 page
│   │   ├── App.jsx             # React Router v6 Routes setup
│   │   ├── index.css           # Tailwind CSS design system configuration
│   │   └── main.jsx            # React 18 Root Renderer
│   ├── tailwind.config.js      # Custom theme tokens & font family definitions
│   └── vite.config.js          # Vite build & dev server config
│
├── server/                     # Backend Express.js Server
│   ├── config/
│   │   └── db.js               # Mongoose MongoDB connection handler
│   ├── controllers/            # Request handlers & business logic
│   │   ├── authController.js   # User registration, login & profile handlers
│   │   ├── productController.js# Catalog search, filter, CRUD endpoints
│   │   ├── orderController.js  # Order placement, status tracking & revenue calculation
│   │   ├── storeController.js  # Vendor store creation & management
│   │   ├── reviewController.js # Verified product review handlers
│   │   └── adminController.js  # Admin metrics & GMV analytics
│   ├── middleware/
│   │   ├── authMiddleware.js   # JWT authentication & role authorization guards
│   │   └── errorMiddleware.js  # Centralized error handler & 404 handler
│   ├── models/                 # Mongoose Data Models & Schemas
│   │   ├── User.js             # User account schema with password hashing
│   │   ├── Vendor.js           # Seller application schema
│   │   ├── Store.js            # Vendor store profile schema
│   │   ├── Product.js          # Product listing schema
│   │   ├── Order.js            # Order schema with delivery state tracking
│   │   └── Review.js           # Customer review schema
│   ├── routes/                 # Express API Route Definitions
│   │   ├── authRoutes.js
│   │   ├── productRoutes.js
│   │   ├── orderRoutes.js
│   │   ├── storeRoutes.js
│   │   ├── reviewRoutes.js
│   │   └── adminRoutes.js
│   ├── seeder.js               # Initial database seeder script
│   └── server.js               # Express application entry point
└── README.md                   # Main project documentation
```

---

## ⚡ Key Highlights
- **100% Responsive UI** built with Tailwind CSS & custom Playfair Display serif typography.
- **JWT Protection** on all sensitive backend routes & roles.
- **Complete E-Commerce Flow** from browsing to checkout & seller fulfillment.

*Updated: August 19, 2026*
