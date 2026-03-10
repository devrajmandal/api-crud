# Quora Posts - RESTful CRUD App

A simple RESTful web application built with Node.js and Express that implements full CRUD (Create, Read, Update, Delete) operations for posts — inspired by Quora.

## Features

- **Create** new posts with username and content
- **Read** all posts or view individual post details
- **Update** post content
- **Delete** posts

## Tech Stack

- **Node.js** with **Express 5.2.1**
- **EJS** for server-side templating
- **UUID** for generating unique post IDs
- **method-override** for HTTP method support (PATCH/DELETE)

## Project Structure

```
REST/
├── index.js          # Main server and routes
├── public/
│   └── style.css     # Stylesheet
├── views/
│   ├── index.ejs     # All posts page
│   ├── new.ejs       # Create new post form
│   ├── show.ejs      # Single post detail page
│   └── edit.ejs      # Edit post form
├── package.json
├── package-lock.json
├── .gitignore
└── README.md
```

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) installed

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/devrajmandal/api-crud.git
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the server:
   ```bash
   node index.js
   ```

4. Open your browser and go to `http://localhost:8080/posts`

## How It Works

- **In-memory storage**: Posts are stored in an array (data is lost when server restarts)
- **RESTful routing**: Follows REST conventions for clean API design
- **Method override**: Uses `method-override` middleware to support PATCH and DELETE methods in HTML forms
- **Sample data**: Comes with 3 pre-loaded sample posts on startup

## API Routes

| Method | Route              | Description                  |
|--------|--------------------|------------------------------|
| GET    | `/posts`           | View all posts               |
| GET    | `/posts/new`       | Form to create a new post    |
| POST   | `/posts`           | Submit a new post            |
| GET    | `/posts/:id`       | View a single post           |
| GET    | `/posts/:id/edit`  | Form to edit a post          |
| PATCH  | `/posts/:id`       | Update a post's content      |
| DELETE | `/posts/:id`       | Delete a post                |

## Usage Flow

1. **View Posts**: Navigate to `/posts` to see all posts
2. **Create Post**: Click "Create New Post" → Fill form → Submit
3. **View Details**: Click on any post to see full details
4. **Edit Post**: Click "Edit" button → Modify content → Submit
5. **Delete Post**: Click "Delete" button to remove a post

## Notes

- Data is stored in memory only. All posts will be reset when the server restarts.
- To persist data, consider integrating a database like MongoDB, PostgreSQL, or SQLite.
- PATCH and DELETE methods in forms are implemented using `method-override` with `?_method=PATCH` and `?_method=DELETE` query parameters.

## Author

**Devraj Mandal**
