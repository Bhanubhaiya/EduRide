# EduRide

This repository contains a full-stack ride-sharing application built with:

- **Backend:** Node.js and Express with MongoDB for data persistence.
- **Frontend:** React application bootstrapped with Vite, styled using Tailwind CSS.

> 🗂 The original project was named *Ripedo*, but it has since been rebranded to **EduRide**.

---

## Project Structure

```
EduRide/
├─ Backend/          # Node.js/Express server
│  ├─ controllers/   # Request handlers
│  ├─ db/            # Database connection
│  ├─ middlewares/   # Auth and other middleware
│  ├─ models/        # Mongoose schemas
│  ├─ routes/        # API route definitions
│  ├─ services/      # Business logic
│  ├─ app.js         # Express app initialization
│  ├─ server.js      # Server entrypoint
│  └─ socket.js      # Socket.io setup

├─ frontend/         # React/Vite frontend
│  ├─ public/        # Static assets
│  ├─ src/           # React source code
│  │  ├─ components/ # Reusable UI components
│  │  ├─ context/    # React context providers
│  │  ├─ pages/      # Route-based pages
│  │  └─ App.jsx      # Root component
│  ├─ package.json
│  └─ vite.config.js

└─ none.txt          # Miscellaneous test file (not part of application logic)
```

## Getting Started

### Prerequisites

- Node.js v16+ (or newer)
- npm or Yarn
- MongoDB running locally or accessible via URI

### Backend Setup

1. Navigate to the `Backend` directory:
   ```bash
   cd Backend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Configure environment variables (create a `.env` file) with values for:
   - `MONGODB_URI` (MongoDB connection string)
   - `JWT_SECRET` (secret for JSON Web Tokens)
   - Any other config used in the code
4. Start the server:
   ```bash
   npm start
   # or for development with nodemon:
   npm run dev
   ```

The backend exposes RESTful endpoints under `/api` and uses Socket.io for real-time features.

### Frontend Setup

1. Change to the `frontend` directory:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the dev server:
   ```bash
   npm run dev
   ```

The UI will be available at `http://localhost:5173` (or another port displayed in the terminal).

## Development Notes

- **Authentication**: Both users and captains are supported; middleware controls protected routes.
- **Realtime**: Socket connections are used for live ride updates.
- **Database**: Uses Mongoose models defined in `models/`.

## Scripts

Each package (`Backend` and `frontend`) has its own `package.json` with scripts. Typical commands:

- `npm start` – run production server
- `npm run dev` – run development server with hot reload

## Contribution

Feel free to open issues or submit pull requests. Please ensure code follows existing style conventions.

---

