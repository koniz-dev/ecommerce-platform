# 🛒 E-commerce Platform

> A complete e-commerce platform with admin dashboard and online store built with Next.js 15 and React 19.

[![Next.js](https://img.shields.io/badge/Next.js-15-black?style=for-the-badge&logo=next.js)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)

## 📋 Overview

This project is a complete e-commerce system consisting of:

- **E-commerce Store** - Online storefront for customers
- **E-commerce Admin** - Admin dashboard for sellers

Both applications are managed as Git submodules in this repository for easy development and maintenance.

## 🏗️ Project Structure

```
ecommerce/
├── ecommerce-store/      # Frontend store (Customer-facing)
│   ├── Next.js 15
│   ├── React 19
│   ├── Tailwind CSS
│   └── Zustand (State Management)
│
└── ecommerce-admin/      # Admin dashboard (Seller-facing)
    ├── Next.js 15
    ├── React 19
    ├── Prisma (ORM)
    ├── Clerk (Authentication)
    ├── Stripe (Payment)
    └── Recharts (Analytics)
```

## ✨ Features

### 🛍️ E-commerce Store
- ✅ Browse and search products
- ✅ Product details view
- ✅ Shopping cart and checkout
- ✅ Order management
- ✅ Modern, responsive UI

### ⚙️ E-commerce Admin
- ✅ Product management (CRUD)
- ✅ Order management
- ✅ Analytics and reports
- ✅ Stripe payment integration
- ✅ Image upload with Cloudinary
- ✅ User authentication with Clerk
- ✅ Data tables with sorting and filtering

## 🚀 Getting Started

### Prerequisites

- Node.js 22.x (for admin) or 20.x and above
- npm, yarn, pnpm, or bun
- Git

### Installation

1. **Clone the repository with submodules:**

```bash
git clone --recurse-submodules https://github.com/koniz-dev/ecommerce.git
cd ecommerce
```

Or if you already cloned:

```bash
git submodule update --init --recursive
```

2. **Install dependencies for Store:**

```bash
cd ecommerce-store
npm install
# or
yarn install
# or
pnpm install
```

3. **Install dependencies for Admin:**

```bash
cd ../ecommerce-admin
npm install
# or
yarn install
# or
pnpm install
```

### Running the Applications

#### Run Store (Port 3000)

```bash
cd ecommerce-store
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

#### Run Admin (Port 3001)

```bash
cd ecommerce-admin
npm run dev
```

Open [http://localhost:3001](http://localhost:3001) in your browser.

> **Note:** Admin uses port 3000 by default. If Store is running, you can change the Admin port by running `PORT=3001 npm run dev`.

### Environment Setup

#### E-commerce Store

Create a `.env.local` file in the `ecommerce-store` directory:

```env
# API endpoints
NEXT_PUBLIC_API_URL=http://localhost:3001/api
```

#### E-commerce Admin

Create a `.env.local` file in the `ecommerce-admin` directory:

```env
# Database
DATABASE_URL="postgresql://user:password@localhost:5432/ecommerce"

# Clerk Authentication
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_key
CLERK_SECRET_KEY=your_clerk_secret

# Stripe
STRIPE_API_KEY=your_stripe_key
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=your_stripe_publishable_key

# Cloudinary
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# App URL
NEXT_PUBLIC_APP_URL=http://localhost:3001
```

Then run Prisma migrations:

```bash
cd ecommerce-admin
npx prisma migrate dev
npx prisma generate
```

## 🛠️ Tech Stack

### Core
- **Next.js 15** - React framework with App Router
- **React 19** - UI library
- **TypeScript** - Type safety
- **Tailwind CSS 4** - Styling

### E-commerce Store
- **Zustand** - State management
- **Axios** - HTTP client
- **Radix UI** - Headless UI components
- **Lucide React** - Icons
- **React Hot Toast** - Notifications

### E-commerce Admin
- **Prisma** - Database ORM
- **Clerk** - Authentication & User management
- **Stripe** - Payment processing
- **React Hook Form** - Form handling
- **Zod** - Schema validation
- **TanStack Table** - Data tables
- **Recharts** - Data visualization
- **Cloudinary** - Image upload & management

## 📝 Available Scripts

### Store

```bash
npm run dev      # Development server
npm run build    # Production build
npm run start    # Start production server
npm run lint     # Lint code
```

### Admin

```bash
npm run dev              # Development server
npm run build            # Build with Prisma generate
npm run start            # Start production server
npm run lint             # Lint code
npm run prisma:setup     # Format, validate & generate Prisma
```

## 🔄 Submodule Management

### Update submodules to latest commits

```bash
git submodule update --remote
```

### Update submodules to specific commits

```bash
cd ecommerce-store
git checkout <commit-hash>
cd ..

cd ecommerce-admin
git checkout <commit-hash>
cd ..
```

### Commit submodule changes

```bash
git add ecommerce-store ecommerce-admin
git commit -m "Update submodules"
```

## 📦 Building for Production

### Store

```bash
cd ecommerce-store
npm run build
npm run start
```

### Admin

```bash
cd ecommerce-admin
npm run build
npm run start
```

## 🤝 Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is private and owned by koniz-dev.

## 🔗 Links

- **Store Repository:** [ecommerce-store](https://github.com/koniz-dev/ecommerce-store)
- **Admin Repository:** [ecommerce-admin](https://github.com/koniz-dev/ecommerce-admin)
- **Live Store:** [ecommerce-store-tau-indol.vercel.app](https://ecommerce-store-tau-indol.vercel.app)

## 👨‍💻 Author

**Koniz Dev**

- GitHub: [@koniz-dev](https://github.com/koniz-dev)

---

⭐ If you find this project useful, please give it a star!
