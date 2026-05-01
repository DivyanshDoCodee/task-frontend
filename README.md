# TaskFlow - Frontend

React-based frontend for the Team Task Manager application with role-based access control, project management, and Kanban board.

## 🚀 Features

- **Authentication** - JWT-based login/signup with protected routes
- **Dashboard** - Overview of projects, tasks, and statistics
- **Projects** - Create and manage projects with team members
- **Kanban Board** - Visual task management (To Do, In Progress, Review, Done)
- **My Tasks** - Personal task view with filters
- **Role-Based UI** - Different permissions for Admins and Members

## 🛠 Tech Stack

- React 18
- React Router v6
- TanStack Query (React Query)
- Axios
- React Hot Toast
- date-fns

## ⚙️ Setup

### Prerequisites
- Node.js 18+
- Backend API running (see [backend repo](https://github.com/DivyanshDoCodee/task))

### Installation

```bash
npm install
```

### Environment Variables

Create a `.env` file in the root directory:

```env
REACT_APP_API_URL=http://localhost:5000/api
```

For production (Railway):
```env
REACT_APP_API_URL=https://your-backend.up.railway.app/api
```

### Development

```bash
npm start
```

Runs on [http://localhost:3000](http://localhost:3000)

### Build

```bash
npm run build
```

Creates optimized production build in the `build/` folder.

## 🌐 Deployment on Railway

1. Create a new Railway project from this repository
2. Add environment variable:
   - `REACT_APP_API_URL` - Your backend Railway URL + `/api`
3. Railway will automatically:
   - Run `npm run build`
   - Serve with `npx serve -s build -l 3000`

## 📁 Project Structure

```
src/
├── components/
│   ├── layout/
│   │   ├── Layout.jsx          # Main layout with sidebar
│   │   └── Layout.css
│   ├── tasks/
│   │   ├── TaskCard.jsx        # Kanban card component
│   │   └── TaskCard.css
│   ├── Modal.jsx               # Reusable modal
│   └── Modal.css
├── context/
│   └── AuthContext.jsx         # Auth state management
├── pages/
│   ├── LoginPage.jsx
│   ├── RegisterPage.jsx
│   ├── DashboardPage.jsx
│   ├── ProjectsPage.jsx
│   ├── ProjectDetailPage.jsx   # Board + List + Members tabs
│   └── MyTasksPage.jsx
├── utils/
│   └── api.js                  # Axios instance with interceptors
├── App.jsx                     # Routes and auth provider
├── index.js                    # Entry point
└── index.css                   # Global styles
```

## 🔗 Related

- [Backend Repository](https://github.com/DivyanshDoCodee/task)

## 📝 License

MIT
