# Quora Posts - RESTful CRUD App

A simple RESTful web application built with Node.js and Express that lets users create, view, and update posts — inspired by Quora.

## Features

- View all posts
- View a single post in detail
- Create a new post (username + content)
- Update post content (via PATCH)

## Tech Stack

- **Node.js** with **Express 5**
- **EJS** for server-side templating
- **UUID** for generating unique post IDs

## Project Structure

```
REST/
├── index.js          # Main server and routes
├── public/
│   └── style.css     # Stylesheet
├── views/
│   ├── index.ejs     # All posts page
│   ├── new.ejs       # Create new post form
│   └── show.ejs      # Single post detail page
├── package.json
└── .gitignore
```

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) installed

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/devrajmandal/api-crud.git
   cd REST
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

## API Routes

| Method | Route           | Description             |
|--------|-----------------|-------------------------|
| GET    | `/posts`        | View all posts          |
| GET    | `/posts/new`    | Form to create a post   |
| POST   | `/posts`        | Submit a new post       |
| GET    | `/posts/:id`    | View a single post      |
| PATCH  | `/posts/:id`    | Update a post's content |

## Author

Devraj
