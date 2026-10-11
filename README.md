# Atmos – Weather Dashboard

### Cognifyz Technologies | Full Stack Development Internship | Level 4 – Task 6

## Overview

**Atmos** is a responsive weather dashboard developed as part of the Cognifyz Technologies Full Stack Development Internship. The application integrates the OpenWeather API to retrieve and display real-time weather information for user-selected cities through a clean, intuitive, and user-friendly interface.

The project demonstrates practical experience in external API integration, asynchronous JavaScript, RESTful API development, server-side request validation, rate limiting, and centralized error handling using Node.js and Express.js.

## Project Objectives

- Integrate a third-party API to retrieve real-time weather information.
  
- Build a responsive and user-friendly weather dashboard.
  
- Develop REST API endpoints using Node.js and Express.js.
  
- Securely manage API credentials using environment variables.
  
- Implement request validation, rate limiting, and structured error handling.
  
- Organize the application using a modular, maintainable project structure.

## Key Features

- **Real-Time Weather Data:** Retrieves current weather conditions for a specified city.
  
- **Temperature Information:** Displays current temperature and feels-like temperature in Celsius.
  
- **Weather Details:** Shows humidity, wind speed, atmospheric pressure, visibility, and weather descriptions.
  
- **Dynamic Weather Icons:** Displays weather icons based on the API response.
  
- **City Search:** Allows users to search for weather conditions by city name.
  
- **Responsive Interface:** Provides a clean dashboard layout suitable for different screen sizes.
  
- **External API Integration:** Connects to the OpenWeather API through a server-side service.
  
- **Input Validation:** Validates city names and handles missing or invalid input.
  
- **Rate Limiting:** Restricts excessive API requests to help protect the application.
  
- **Centralized Error Handling:** Provides meaningful error responses for invalid requests and external service failures.
  
- **Environment-Based Configuration:** Keeps API credentials outside the source code using a `.env` file.

## Technology Stack

| Technology         | Purpose                                                 |
| ------------------ | ------------------------------------------------------- |
| HTML5              | Defines the structure of the application                |
| CSS3               | Provides styling and responsive layout                  |
| JavaScript         | Handles frontend interactions and asynchronous requests |
| Node.js            | Runs JavaScript on the server side                      |
| Express.js         | Creates the web server and manages REST API routes      |
| OpenWeather API    | Provides real-time weather data                         |
| dotenv             | Manages environment variables and API credentials       |
| express-rate-limit | Limits API requests to help prevent excessive traffic   |
| Git                | Tracks code changes and manages version history         |
| GitHub             | Hosts the project repository and supports collaboration |

## Application Architecture

The application follows a modular architecture that separates the user interface, routes, controllers, external API communication, and middleware.

- **Frontend:** Collects city input and displays weather information.
  
- **Routes:** Defines the weather API endpoint.

- **Controllers:** Validates incoming requests and coordinates responses.

- **Services:** Communicates with the OpenWeather API and processes weather data.
  
- **Middleware:** Implements rate limiting and centralized error handling.

- **Configuration:** Loads environment variables and server settings.

## Project Structure


Level4_Task7/
│
├── config/
│   └── env.js
│
├── controllers/
│   └── apiController.js
│
├── middleware/
│   ├── errorHandler.js
│   └── rateLimiter.js
│
├── public/
│   ├── index.html
│   ├── css/
│   │   └── style.css
│   └── js/
│       └── app.js
│
├── routes/
│   └── apiRoutes.js
│
├── services/
│   └── weatherService.js
│
├── .env
├── .env.example
├── .gitignore
├── package.json
├── package-lock.json
├── server.js
└── README.md


## Installation and Setup

### Prerequisites

- Node.js and npm
  
- A code editor such as Visual Studio Code

- An OpenWeather API account and API key

### 1. Clone the Repository


git clone <https://github.com/gundavarshini>

cd Level4_Task7


Replace the repository URL with your actual GitHub repository URL.

### 2. Install Dependencies


npm install


### 3. Configure Environment Variables

Create a `.env` file in the project root directory:


PORT=5000

WEATHER_API_KEY=your_actual_openweather_api_key


Obtain your API key from [OpenWeather](https://openweathermap.org/api).

Replace the placeholder with your actual API key. Do not commit the `.env` file or expose your API key in public repositories.

### 4. Start the Application


npm start


For development, if supported by your Node.js setup, run:

npm run dev


### 5. Open the Dashboard

Visit the following URL in your browser:


http://localhost:5000


## API Endpoints

| HTTP Method | API Endpoint                  | Description                                                  |
| ----------- | ----------------------------- | ------------------------------------------------------------ |
| GET         | `/api/health`                 | Checks whether the application server is running             |
| GET         | `/api/weather?city=Hyderabad` | Retrieves current weather information for the specified city |


### Example Request


GET /api/weather?city=Hyderabad


### Example Response

{
  "success": true,
  "data": {
    "city": "Hyderabad",
    "country": "IN",
    "temperature": 34,
    "feelsLike": 34,
    "humidity": 45,
    "pressure": 1012,
    "description": "clear sky",
    "icon": "01d",
    "windSpeed": 3.5,
    "visibility": 10000
  }
}


*Note: The values above are illustrative. Actual weather data depends on the API response and current conditions.*

## Error Handling and Reliability

The application incorporates several safeguards:

- Validates city names before making external API requests.

- Handles cities that cannot be found.
  
- Detects invalid API credentials and external service failures.

- Uses a request timeout to prevent waiting indefinitely for the weather provider.
  
- Applies rate limiting to reduce excessive requests.
  
- Returns structured JSON responses for API errors.
  
- Keeps sensitive configuration out of committed source code.

## Security Considerations

- API credentials are stored in environment variables.
  
- The `.env` file is excluded through `.gitignore`.
  
- The frontend communicates with the application's backend rather than exposing the API key in browser code.
  
- Request payloads and input lengths are restricted where applicable.
  
- Rate limiting helps reduce abusive API traffic.

## Skills Demonstrated

Through this project, I gained practical experience with:

- Third-party REST API integration
  
- Node.js and Express.js backend development
  
- Asynchronous programming with `async/await` and `fetch`
  
- REST endpoint design and HTTP status codes
  
- Environment-based configuration
  
- Middleware implementation
  
- Request validation and error handling.
  
- Responsive frontend development
  
- Modular application architecture
  
- Git and GitHub project documentation

## Learning Outcomes

This project strengthened my understanding of how frontend applications communicate with backend services and how backend systems consume external APIs. It also provided hands-on experience in structuring an application for maintainability, protecting API credentials, managing failed requests, and implementing basic API reliability measures.

## Future Enhancements

- Five-day weather forecasts
  
- Automatic location-based weather information
  
- Recent search history and favorite cities
  
- Temperature unit conversion between Celsius and Fahrenheit
  
- Weather trend visualizations
  
- Automated testing and deployment
  
- CI/CD integration

## Acknowledgment

This project was developed as part of the **Full Stack Development Internship at Cognifyz Technologies**, under Level 4 – Task 7: Advanced API Usage and External API Integration.

## Author

**Varshini Reddy**

GitHub: [https://github.com/gundavarshini](https://github.com/)


