# Setup Guide - Heal Pharma Website

## Prerequisites
- Node.js v16+ or Python 3.9+
- Git
- npm or yarn
- Database system (MongoDB or PostgreSQL)

## Local Development Setup

### 1. Clone the Repository
```bash
git clone https://github.com/healpharma01-arch/Heal-pharma.git
cd Heal-pharma
```

### 2. Frontend Setup (React/Next.js)
```bash
cd frontend
npm install
cp .env.example .env.local
npm run dev
```

The frontend will be available at `http://localhost:3000`

### 3. Backend Setup (Node.js/Express)
```bash
cd ../backend
npm install
cp .env.example .env
npm run dev
```

The API will run on `http://localhost:5000`

### 4. Database Setup
Configure your database connection in `.env`:
```
DB_URL=mongodb://localhost:27017/heal-pharma
# or
DB_URL=postgresql://user:password@localhost:5432/heal-pharma
```

### 5. Environment Variables
Create `.env` files with required variables:
```
# Frontend
REACT_APP_API_URL=http://localhost:5000/api

# Backend
PORT=5000
DB_URL=your_database_url
JWT_SECRET=your_secret_key
STRIPE_KEY=your_stripe_key
```

## Database Initialization
```bash
npm run migrate
npm run seed  # Load sample products
```

## Running Tests
```bash
npm test
npm run test:coverage
```

## Building for Production
```bash
# Frontend
cd frontend
npm run build

# Backend
cd ../backend
npm run build
```

## Deployment
See [DEPLOYMENT.md](./DEPLOYMENT.md) for deployment instructions.

---
For issues or questions, open an issue on GitHub.
