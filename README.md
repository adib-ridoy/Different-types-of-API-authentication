# API Authentication Project

A Node.js Express application demonstrating different types of API authentication methods including No Auth, Basic Auth, API Key, and Bearer Token authentication.

## Features

- **No Authentication**: Fetch random secrets without authentication
- **Basic Authentication**: Access paginated secrets using username/password
- **API Key Authentication**: Filter secrets by score using an API key
- **Bearer Token Authentication**: Access specific secrets using bearer tokens

## Technologies Used

- Node.js
- Express.js
- Axios
- EJS (Embedded JavaScript templates)

## Prerequisites

- Node.js installed on your machine
- npm (Node Package Manager)

## Installation

1. Clone or download the project
2. Navigate to the project directory:
   ```bash
   cd "2. Back-End/5.4 API Authentication"
   ```
3. Install dependencies:
   ```bash
   npm install
   ```

## Configuration

Before running the application, update the authentication credentials in `index.js`:

```javascript
const yourUsername = "your_username_here";
const yourPassword = "your_password_here";
const yourAPIKey = "your_api_key_here";
const yourBearerToken = "your_bearer_token_here";
```

Replace these values with your actual credentials from the Secrets API.

## Running the Application

### Using Node:
```bash
node index.js
```

### Using Nodemon (for development):
```bash
nodemon index.js
```

The server will start on `http://localhost:3000`

## API Endpoints

### 1. Home
- **URL**: `/`
- **Method**: GET
- **Description**: Displays the home page

### 2. No Authentication
- **URL**: `/noAuth`
- **Method**: GET
- **Description**: Fetches a random secret without authentication

### 3. Basic Authentication
- **URL**: `/basicAuth`
- **Method**: GET
- **Description**: Fetches all secrets from page 2 using basic authentication
- **Requires**: Valid username and password

### 4. API Key Authentication
- **URL**: `/apiKey`
- **Method**: GET
- **Description**: Filters secrets with embarrassment score ≥ 5
- **Requires**: Valid API key

### 5. Bearer Token Authentication
- **URL**: `/bearerToken`
- **Method**: GET
- **Description**: Fetches a specific secret by ID (ID: 42)
- **Requires**: Valid bearer token

## External API

This project uses the Secrets API:
- **Base URL**: `https://secrets-api.appbrewery.com/`

## Project Structure

```
5.4 API Authentication/
├── node_modules/
├── views/
│   └── index.ejs
├── .gitignore
├── index.js
├── package.json
├── package-lock.json
└── README.md
```

## Dependencies

- **express**: ^4.18.2 - Web framework for Node.js
- **axios**: ^1.4.0 - Promise-based HTTP client
- **ejs**: ^3.1.9 - Template engine

## Troubleshooting

### Basic Authentication Failed
- Ensure your username and password are correct
- Verify the API endpoint is accessible
- Check if credentials need to be registered with the API first

### Connection Errors
- Verify your internet connection
- Check if the API server is operational
- Ensure no firewall is blocking the requests

## License

ISC

## Author

Created as part of a web development course project.
