# Summer-Training-Project

TaskFlow Pro – Advanced Full-Stack Task Management App

📝 Project Description:
A fully featured full-stack task management application that supports user authentication, task CRUD, role-based access, and a modern UI with enhanced features like filtering, due dates, priority tags, dark mode, and drag-and-drop functionality.

🧰 Tech Stack:
Layer	Technology
Frontend	React.js, Tailwind CSS / Material UI, React DnD
State Mgmt	React Context / Redux (for auth and tasks)
Backend	Node.js, Express.js
Database	MongoDB (Mongoose ODM)
Auth	JWT + bcrypt.js
Hosting	Vercel (Frontend), Render/Railway (Backend), MongoDB Atlas (Database)

🔐 Authentication & Authorization:
JWT-based authentication with session persistence

Role-based access control (Admin/User)

Admin: Can manage all users and tasks

User: Can only manage their own tasks

Password encryption using bcrypt

✅ Core Features:
User Auth:
Register/Login/Logout

Token-based access

Profile fetch

Task CRUD:
Create, Read, Update, Delete user tasks

REST API with proper HTTP methods

Backend validation with Mongoose schemas

🌟 Bonus Features (Implemented):
Feature	Description
✅ Task Due Dates	Add a due date when creating/editing a task
✅ Priority Tagging	Choose between Low, Medium, High
✅ Filters	Filter tasks by status (Pending/Completed) or priority
✅ Dark Mode	Toggle switch to switch themes (CSS/JS toggle or Tailwind)
✅ Mobile Responsive UI	Fully functional on smartphones/tablets
✅ Drag-and-Drop	Reorder tasks via react-beautiful-dnd or react-dnd
✅ Role-Based Access	Separate access and controls for Admin and Users

🧪 Sample Task Schema (Mongoose):
js
Copy
Edit
{
  title: String,
  description: String,
  dueDate: Date,
  priority: { type: String, enum: ['Low', 'Medium', 'High'] },
  status: { type: String, enum: ['Pending', 'In Progress', 'Completed'] },
  order: Number, // for drag-and-drop sorting
  user: mongoose.Schema.Types.ObjectId,
  createdAt: Date,
  updatedAt: Date
}
📱 Frontend Pages:
Login / Register / Logout

Dashboard

List of tasks

Filter & Search

Drag & drop

Add/Edit Task Modal

Theme toggle

Admin Panel

View all users

Delete users

Manage all tasks

📦 API Routes (Express.js):
Route	Method	Description
/api/auth/register	POST	Register new user
/api/auth/login	POST	Login user
/api/tasks/	GET	Get all tasks for user/admin
/api/tasks/	POST	Create task
/api/tasks/:id	PUT	Update task
/api/tasks/:id	DELETE	Delete task
/api/admin/users	GET	(Admin) List all users
/api/admin/tasks	GET	(Admin) List all tasks

🌐 Deployment Plan:
Component	Platform
Frontend	Vercel
Backend	Railway / Render
Database	MongoDB Atlas
ENV Config	.env files (with Vercel/Render settings)

📄 Deliverables:
✅ Deployed Web App Link

✅ GitHub Repositories (Frontend & Backend)

✅ README Files with:

Tech stack

Setup instructions

Live link

API usage

Screenshots

✅ PDF Documentation:

Architecture diagram

ER Diagram

Features list with screenshots

Future feature roadmap


