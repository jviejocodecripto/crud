# Task CRUD Application

A simple yet powerful Task CRUD application built with **Next.js** and **MongoDB**. No authentication required.

## Features

- ✅ **Create** tasks with title and description
- ✅ **Read** all tasks from MongoDB
- ✅ **Update** tasks (title, description, completion status)
- ✅ **Delete** tasks
- ✅ Mark tasks as completed/incomplete
- ✅ Clean and modern UI with Tailwind CSS
- ✅ MongoDB native driver integration

## Prerequisites

- **Node.js** 18+ installed
- **MongoDB** running locally on `mongodb://localhost:27017`
- npm or yarn

## Installation

1. Clone the repository:
```bash
git clone https://github.com/jviejocodecripto/crud.git
cd crud
```

2. Install dependencies:
```bash
npm install
```

3. Configure MongoDB (optional):
   - Edit `.env.local` if you need to use a different MongoDB URI or database name
   - Default: `MONGODB_URI=mongodb://localhost:27017` and `MONGODB_DB=crud-db`

## Running the Application

```bash
npm run dev
```

The application will be available at `http://localhost:3000`

## Building for Production

```bash
npm run build
npm start
```

## Project Structure

```
crud/
├── app/
│   ├── api/
│   │   └── tasks/
│   │       ├── route.ts          # GET & POST endpoints
│   │       └── [id]/route.ts      # PUT & DELETE endpoints
│   ├── layout.tsx
│   ├── page.tsx                  # Main page with CRUD UI
│   └── globals.css
├── lib/
│   └── mongodb.ts                # MongoDB connection helper
├── .env.local                    # Environment variables
├── package.json
└── tsconfig.json
```

## API Endpoints

### Get all tasks
```
GET /api/tasks
```

### Create a task
```
POST /api/tasks
Content-Type: application/json

{
  "title": "Task Title",
  "description": "Task Description (optional)"
}
```

### Update a task
```
PUT /api/tasks/:id
Content-Type: application/json

{
  "title": "Updated Title",
  "description": "Updated Description",
  "completed": true
}
```

### Delete a task
```
DELETE /api/tasks/:id
```

## Technologies Used

- **Next.js** - React framework for production
- **TypeScript** - Static type checking
- **MongoDB** - NoSQL database with native driver
- **Tailwind CSS** - Utility-first CSS framework
- **React Hooks** - State management

## Repository Links

- **GitHub**: https://github.com/jviejocodecripto/crud
- **GitLab**: https://gitlab.codecrypto.academy/jviejo/crud

## License

MIT License
