# 📝 Real-Time WebSocket Kanban Board

A modern, full-stack Kanban board application built for real-time collaboration. This project features a drag-and-drop interface, task synchronization across multiple clients using WebSockets, and comprehensive testing coverage.

## 🚀 Features

- **Real-Time Collaboration**: Instant task updates across all connected clients using Socket.IO.
- **Interactive Kanban Board**: Smooth drag-and-drop functionality to move tasks between stages (To Do, In Progress, Done).
- **Task Management**: Create, update, and delete tasks with ease.
- **Categorization & Priority**: Assign categories (Bug, Feature, Enhancement) and priority levels (Low, Medium, High) to tasks.
- **File Attachments**: Support for uploading images and documents to tasks with image previews.
- **Progress Analytics**: Real-time charts visualizing task distribution and completion percentage.
- **Secure Authentication**: User management powered by Clerk.
- **Modern UI**: Responsive and accessible design built with Chakra UI and Framer Motion.

## 🛠 Tech Stack

### Frontend
- **React 19**: Modern UI library.
- **Chakra UI**: Accessible component library for styling.
- **Socket.IO Client**: Real-time communication.
- **Hello Pangea DnD**: Accessible drag-and-drop.
- **Recharts**: Responsive data visualization.
- **Clerk**: Authentication and user management.

### Backend
- **Node.js & Express**: Robust server-side framework.
- **Socket.IO**: WebSocket server for real-time events.
- **MongoDB & Mongoose**: Scalable NoSQL database and ODM.
- **Dotenv**: Environment variable management.

### Testing
- **Vitest**: Fast unit and integration testing.
- **React Testing Library**: Testing UI components.
- **Playwright**: Reliable end-to-end testing across browsers.

---

## 📂 Project Structure

```
websocket-kanban-vitest-playwright
│── backend/                     # Node.js WebSocket server
│   ├── models/                  # Mongoose schemas
│   ├── server.js                 # Express + Socket.IO setup
│   └── .env.example             # Template for backend environment variables
│
│── frontend/                     # React application
│   ├── src/
│   │   ├── components/           # Reusable UI components
│   │   ├── theme.js              # Chakra UI theme configuration
│   │   └── App.jsx               # Main application logic
│   ├── tests/                    # Vitest and Playwright tests
│   └── .env.example             # Template for frontend environment variables
│
└── README.md                     # Project documentation
```

---

## 🚦 Getting Started

### Prerequisites
- Node.js (v18+)
- MongoDB (Local or Atlas)

### 1. Backend Setup
1. Navigate to the `backend` directory:
   ```bash
   cd backend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file based on `.env.example` and add your MongoDB URI:
   ```env
   PORT=5000
   MONGODB_URI=your_mongodb_uri
   ALLOWED_ORIGINS=http://localhost:5173
   ```
4. Start the server:
   ```bash
   npm start
   ```

### 2. Frontend Setup
1. Navigate to the `frontend` directory:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env.local` file and add your Clerk publishable key:
   ```env
   VITE_CLERK_PUBLISHABLE_KEY=your_clerk_pub_key
   VITE_API_URL=http://localhost:5000
   ```
4. Run the development server:
   ```bash
   npm run dev
   ```

---

## 🧪 Testing

### Unit & Integration Tests (Vitest)
To run the frontend tests:
```bash
cd frontend
npm test
```

### End-to-End Tests (Playwright)
To run E2E tests:
```bash
cd frontend
npx playwright install # If running for the first time
npm run test:e2e
```

---

## 📜 License
This project is open-source and available under the MIT License.
