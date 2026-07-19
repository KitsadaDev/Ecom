# E-commerce Web Application (E-com)

A full-stack e-commerce web application featuring a modern React frontend and a robust Express.js backend powered by Prisma ORM.

## Tech Stack

### Frontend (Client)
- **Core:** React 19, Vite, React Router DOM 7
- **Styling:** Tailwind CSS v4
- **State Management:** Zustand
- **Form Handling:** React Hook Form + Zod validation
- **HTTP Client:** Axios
- **Payment Integration:** Stripe React SDK
- **UI Components:** Swiper, Lucide React, RC-Slider, React Toastify

### Backend (Server)
- **Core:** Node.js, Express.js
- **Database ORM:** Prisma (configured with Supabase / PostgreSQL)
- **Authentication:** JSON Web Tokens (JWT) & BcryptJS
- **Image Storage:** Cloudinary
- **Payment Processing:** Stripe Node SDK
- **Logging:** Morgan

---

## Directory Structure

```text
E-com/
├── client/          # Frontend application (Vite + React)
└── server/          # Backend API service (Express + Prisma)
```

---

## Getting Started

### Prerequisites
Make sure you have [Node.js](https://nodejs.org/) or [Bun](https://bun.sh/) installed.

### 1. Server Setup

Navigate to the `server` directory:
```bash
cd server
```

Install the dependencies:
```bash
npm install
# or if using Bun
bun install
```

Create a `.env` file in the `server` directory and add the following environment variables:
```env
DATABASE_URL="your-postgresql-database-url"
DIRECT_URL="your-postgresql-direct-url" # For Supabase direct connection
JWT_SECRET="your-jwt-secret-key"
CLOUDINARY_CLOUD_NAME="your-cloudinary-cloud-name"
CLOUDINARY_API_KEY="your-cloudinary-api-key"
CLOUDINARY_API_SECRET="your-cloudinary-api-secret"
STRIPE_SECRET_KEY="your-stripe-secret-key"
```

Run database migrations:
```bash
npx prisma migrate dev
```

Start the development server:
```bash
npm run dev
# or
bun run dev
```

---

### 2. Client Setup

Navigate to the `client` directory:
```bash
cd ../client
```

Install the dependencies:
```bash
npm install
# or if using Bun
bun install
```

Start the Vite development server:
```bash
npm run dev
# or
bun run dev
```

The application will be running at `http://localhost:5173`.

---

## Key Features

- **Authentication & Security:** Secure user login and registration with Bcrypt encryption and JWT tokens. Route protection for regular users and administrators.
- **Product Management:** Admin dashboard to create, read, update, and delete products, including category management.
- **Image Management:** Direct image uploads to Cloudinary with automatic resizing and optimization.
- **Search & Filters:** Real-time product search with filtering options by category and price range.
- **Shopping Cart & Checkout:** Comprehensive cart system with checkout summary page.
- **Stripe Payments:** Fully integrated Stripe Checkout for processing credit card payments securely.
- **Order Management:** Tracking order status and history for users, with admin controls to update orders.
