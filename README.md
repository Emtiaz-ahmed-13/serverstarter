# Express TypeScript PostgreSQL Starter

A professional-grade starter template for building high-performance REST APIs using Express.js, PostgreSQL, Prisma ORM, and TypeScript. This boilerplate includes essential features like authentication, validation, and error handling out of the box.

## 🚀 Key Features

- **TypeScript Core**: Full type safety and modern JavaScript features.
- **Prisma ORM**: Type-safe database access with PostgreSQL.
- **Authentication**: JWT-based authentication flow implemented.
- **Validation**: Request body and parameter validation using **Zod**.
- **Security**: CORS enabled, rate-limiting implemented, and environment variable protection.
- **Error Handling**: Standardized global error handling with custom `ApiError` class.
- **Deployment Ready**: Configuration for Vercel included.

## 🛠️ Tech Stack

- **Backend**: Node.js, Express.js
- **Language**: TypeScript
- **Database**: PostgreSQL
- **ORM**: Prisma
- **Validation**: Zod
- **Authentication**: JsonWebToken (JWT), Bcrypt

## 📋 Prerequisites

Ensure you have the following installed:
- Node.js (v18.x or higher)
- PostgreSQL
- npm or yarn

## ⚙️ Getting Started

### 1. Clone the Repository
```bash
git clone <repository-url>
cd serverstarter
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Environment Configuration
Create a `.env` file from `.env.sample`:
```bash
cp .env.sample .env
```
Update the following variables in `.env`:
- `DATABASE_URL`: Your PostgreSQL connection string.
- `JWT_ACCESS_SECRET`: Secret for access tokens.
- `JWT_REFRESH_SECRET`: Secret for refresh tokens.
- `PORT`: (Default: 5000)

### 4. Database Setup
Generate Prisma client and run migrations:
```bash
npx prisma generate
npx prisma migrate dev
```

### 5. Start Development Server
```bash
npm run dev
```

## 📜 Available Scripts

| Script | Description |
| :--- | :--- |
| `npm run dev` | Runs the app in development mode with hot-reload. |
| `npm run build` | Compiles TypeScript to JavaScript in the `dist/` folder. |
| `npm start` | Runs the compiled production build from `dist/`. |
| `npm run postinstall` | Automatically generates Prisma client after installs. |

## 📂 Project Structure

```text
src/
├── app/
│   ├── errors/           # Custom error classes
│   ├── middleware/       # Global and local middlewares
│   ├── modules/          # Business logic (Auth, etc.)
│   ├── routes/           # API Route definitions
│   └── shared/           # Shared utilities and types
├── config/               # Configuration files (env, etc.)
├── helpers/              # Helper functions
├── app.ts                # App initialization
└── server.ts             # Server entry point
```

## 🔒 API Endpoints (Auth Example)

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/api/v1/auth/login` | Authenticates a user and returns tokens. |

## 📄 License

This project is licensed under the [ISC License](LICENSE).
