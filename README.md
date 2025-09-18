# Task Management Web App

A modern, full-stack task management application built with Next.js, MongoDB Atlas, and TypeScript.

## Features

- **User Authentication**: Secure login and signup system
- **Task Management**: Full CRUD operations for tasks
- **Search & Filter**: Real-time search with status filtering (All, Pending, Done)
- **Pagination**: Efficient data loading with pagination support
- **Responsive Design**: Dark theme with professional UI
- **Real-time Updates**: Instant task status changes
- **Dashboard**: Overview with task statistics and recent activity

## Tech Stack

- **Frontend**: Next.js 14, React 19, TypeScript
- **Backend**: Next.js API Routes
- **Database**: MongoDB Atlas
- **Styling**: Tailwind CSS v4, shadcn/ui components
- **Icons**: Lucide React

## Getting Started

### Prerequisites

- Node.js 18+ 
- MongoDB Atlas account
- npm or yarn

### Installation

1. Clone the repository
2. Install dependencies:
   \`\`\`bash
   npm install
   \`\`\`

3. Set up environment variables:
   \`\`\`bash
   cp .env.example .env.local
   \`\`\`
   
   Update `.env.local` with your MongoDB Atlas connection string:
   \`\`\`
   MONGODB_URI=mongodb+srv://<username>:<password>@<cluster-url>/<database-name>?retryWrites=true&w=majority
   \`\`\`

4. Run the development server:
   \`\`\`bash
   npm run dev
   \`\`\`

5. Open [http://localhost:3000](http://localhost:3000) in your browser

## Database Schema

### Tasks Collection
\`\`\`javascript
{
  _id: ObjectId,
  title: String,
  description: String,
  status: "pending" | "completed",
  dueDate: String | null,
  createdAt: String,
  updatedAt: String,
  userId: String
}
\`\`\`

## API Endpoints

- `GET /api/tasks` - Get tasks with search, filter, and pagination
- `POST /api/tasks` - Create a new task
- `PUT /api/tasks/[id]` - Update a task
- `DELETE /api/tasks/[id]` - Delete a task

## Features Overview

### Search & Filter System
- **Search**: Real-time search across task titles and descriptions
- **Filter**: Three-state filtering (All, Pending, Done)
- **Combined**: Search and filter work together seamlessly

### Task Management
- Create tasks with title, description, and optional due date
- Update task status between Pending and Done
- Edit task details
- Delete tasks
- View creation date and time for each task

### Dashboard
- Task statistics overview
- Recent tasks display
- Upcoming deadlines tracking

## Deployment

The app is ready for deployment on Vercel:

1. Push your code to GitHub
2. Connect your repository to Vercel
3. Add your MongoDB Atlas connection string to Vercel environment variables
4. Deploy!

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request
