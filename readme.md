
# Node.js Service Mocking Demo

This project is part of the "Introduction to Node.js" (LFW111) course, focusing on exploring service mocking techniques.

## Project Overview

This simple web application demonstrates how to set up a client-side application that will later be connected to mock services. The current implementation uses hardcoded product data that will eventually be replaced with data from mock services.

## Project Structure

```
node-mocking/
├── static/
│   ├── index.html    # Frontend UI with product display layout
│   └── app.js        # JavaScript functionality using Web Components
└── readme.md         # Project documentation
```

## Setup Instructions

1. Install the serve package globally:
   ```bash
   npm install -g serve
   ```

2. Start the file server:
   ```bash
   serve -p 5050 static
   ```

3. Open your browser and navigate to http://localhost:5050

4. Click the "Fetch Products" button to display product data

## Implementation

The application displays product information from hardcoded data in the app.js file using Web Components. When the "**Fetch Products**" button is clicked, the application:

1. Creates a custom web component (`<product-item>`) for each product
2. Populates the component with product data (name, price, and description)
3. Displays the products in an expandable details/summary format

The implementation leverages modern web technologies:
- Custom Elements API for creating reusable components
- Shadow DOM for style encapsulation
- HTML templates and slots for content projection