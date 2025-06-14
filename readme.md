# Node.js Service Mocking Demo

This project is part of the "Introduction to Node.js" (LFW111) course by The Linux Foundation, focusing on exploring service mocking techniques.

## Project Overview

This application demonstrates how to create a full-stack JavaScript application with a frontend consuming data from a mock backend service. The project implements a product catalog that allows users to:

- Browse products by category (electronics or confectionery)
- View detailed product information
- Add new products to the catalog

## Project Structure

```
node-mocking/
├── mock-srv/               # Backend mock service (Fastify)
│   ├── app.js              # Main application entry point
│   ├── plugins/            # Fastify plugins
│   │   ├── data-utils.js   # Data manipulation utilities
│   │   ├── sensible.js     # Error handling utilities
│   │   └── support.js      # Helper functions
│   └── routes/             # API endpoints
│       ├── confectionery/  # Confectionery products API
│       ├── electronics/    # Electronics products API
│       └── example/        # Example route
├── static/                 # Frontend application
│   ├── index.html          # HTML layout and structure
│   └── app.js              # Frontend JavaScript with Web Components
└── readme.md               # Project documentation
```

## Setup Instructions

### Backend Setup

1. Install dependencies for the mock service:
   ```bash
   cd mock-srv
   npm install
   ```

2. Start the development server:
   ```bash
   npm run dev
   ```

   The backend API will be available at http://localhost:3000

### Frontend Setup

1. Install the serve package globally (if not already installed):
   ```bash
   npm install -g serve
   ```

2. Start the static file server:
   ```bash
   serve -p 5050 static
   ```

3. Open your browser and navigate to http://localhost:5050

## How It Works

1. The frontend application connects to the backend API at http://localhost:3000
2. Users select a product category from the dropdown menu
3. The application fetches products for the selected category from the backend
4. Products are displayed as expandable items with name, price, and description
5. Users can add new products by filling out the form that appears after selecting a category

## Technologies Used

- **Frontend**:
  - Modern JavaScript (ES6+)
  - Custom Elements API for Web Components
  - Shadow DOM for style encapsulation
  - HTML Templates and Slots for content projection

- **Backend**:
  - Node.js
  - Fastify framework for efficient API development
  - Fastify plugins for cross-cutting concerns
  - Automated testing with Node's built-in test runner

## Acknowledgements

- The Linux Foundation for providing the "Introduction to Node.js" (LFW111) course materials and guidance
- Fastify for its high-performance web framework
- Serve for serving static files easily