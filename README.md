# Finance App

A finance tracking application built with FastAPI and React. This application allows users to track their income and expenses with a clean and intuitive interface.

## 🚀 Features

- Track income and expenses
- Categorize transactions
- Add descriptions to transactions
- View transaction history
- Real-time updates
- Responsive design with Bootstrap

## 🛠️ Technology Stack

### Backend
- **FastAPI**: Modern, fast web framework for building APIs with Python
- **SQLAlchemy**: SQL toolkit and ORM
- **SQLite**: Lightweight database
- **Pydantic**: Data validation using Python type annotations
- **CORS Middleware**: For handling cross-origin requests

### Frontend
- **React**: Frontend library for building user interfaces
- **Axios**: HTTP client for making API requests
- **Bootstrap**: CSS framework for responsive design

## 📁 Project Structure

```
FastAPI_Finance/
├── FastAPI/                 # Backend directory
│   ├── main.py             # FastAPI application and routes
│   ├── models.py           # Database models
│   ├── database.py         # Database configuration
│   └── finance.db          # SQLite database
│
└── react/                  # Frontend directory
    └── finance-app/
        ├── src/
        │   ├── App.js      # Main React component
        │   ├── api.js      # API configuration
        │   └── ...
        └── public/
            └── index.html
```

## 🔧 Setup and Installation

### Backend Setup

1. Navigate to the FastAPI directory:
   ```bash
   cd FastAPI
   ```

2. Install Python dependencies:
   ```bash
   pip install fastapi uvicorn sqlalchemy
   ```

3. Start the FastAPI server:
   ```bash
   uvicorn main:app --reload
   ```
   The API will be available at `http://localhost:8000`

### Frontend Setup

1. Navigate to the React app directory:
   ```bash
   cd react/finance-app
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the React development server:
   ```bash
   npm start
   ```
   The application will open at `http://localhost:3000`

## 🌐 API Endpoints

### GET /transactions/
- Retrieves all transactions
- Query Parameters:
  - skip (optional): Number of records to skip
  - limit (optional): Maximum number of records to return

### POST /transactions/
- Creates a new transaction
- Request Body:
  ```json
  {
    "amount": float,
    "category": string,
    "description": string,
    "is_income": boolean,
    "date": string
  }
  ```

## 💾 Database Schema

### Transaction Table
- `id`: Integer (Primary Key)
- `amount`: Float
- `category`: String
- `description`: String
- `is_income`: Boolean
- `date`: String

## 🎯 Future Enhancements

1. User authentication and authorization
2. Transaction categories management
3. Data visualization with charts and graphs
4. Export functionality for transactions
5. Advanced filtering and sorting options
6. Dark mode support
