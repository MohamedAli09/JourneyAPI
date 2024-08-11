 
 
 

 
# Journey API

This API is designed for managing tour operations, including user authentication, booking reviews, and tour management. It's built with Node.js, Express, and MongoDB, providing a robust and scalable solution for tour-based applications.

## Live Preview

You can view the live API in action at [this link](http://hakuna-matata.balloapi.online/).


## Features

- **User Authentication**: Secure user registration and login using JWT.
- **Tour Management**: Create, update, delete, and view tours.
- **Review Management**: Users can leave reviews for tours.
- **Advanced Filtering and Sorting**: Powerful query capabilities for tours.
- **Email Notifications**: Automated email notifications for various actions.

## Project Structure

The project is organized as follows:

```plaintext
after-section-11/
│
├── controllers/            # Controllers for handling API requests
│   ├── authController.js
│   ├── errorController.js
│   ├── handlerFactory.js
│   ├── reviewController.js
│   ├── tourController.js
│   └── userController.js
│
├── models/                 # Mongoose models for MongoDB
│   ├── reviewModel.js
│   ├── tourModel.js
│   └── userModel.js
│
├── routes/                 # Routes for different resources
│   ├── reviewRoutes.js
│   ├── tourRoutes.js
│   └── userRoutes.js
│
├── utils/                  # Utility functions and classes
│   ├── apiFeatures.js
│   ├── appError.js
│   ├── catchAsync.js
│   └── email.js
│
├── app.js                  # Main application setup
├── server.js               # Server configuration and startup
├── config.env              # Environment variables
├── package.json            # Project dependencies and scripts
└── .eslintrc.json          # ESLint configuration
└── .prettierrc             # Prettier configuration
```

## Getting Started

### Prerequisites

- Node.js
- MongoDB

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/Journey-api.git
    cd Journey-api
    ```

2. Install the dependencies:
    ```bash
    npm install
    ```

3. Set up environment variables:
    Create a `config.env` file in the root directory and add your environment variables. Here's an example:

    ```plaintext
    NODE_ENV=development
    DATABASE=mongodb+srv://<username>:<password>@cluster0.mongodb.net/Journey?retryWrites=true&w=majority
    JWT_SECRET=your_jwt_secret
    EMAIL_USERNAME=your_email_username
    EMAIL_PASSWORD=your_email_password
    EMAIL_HOST=your_email_host
    EMAIL_PORT=your_email_port
    ```

4. Start the development server:
    ```bash
    npm start
    ```

## Usage

The API provides endpoints for managing users, tours, and reviews. Below are some of the key endpoints:

- **User Authentication**
    - `POST /api/v1/users/signup`: Register a new user
    - `POST /api/v1/users/login`: Login a user

- **Tours**
    - `GET /api/v1/tours`: Get all tours
    - `POST /api/v1/tours`: Create a new tour
    - `GET /api/v1/tours/:id`: Get a specific tour
    - `PATCH /api/v1/tours/:id`: Update a tour
    - `DELETE /api/v1/tours/:id`: Delete a tour

- **Reviews**
    - `GET /api/v1/reviews`: Get all reviews
    - `POST /api/v1/reviews`: Create a new review
    - `GET /api/v1/reviews/:id`: Get a specific review
    - `PATCH /api/v1/reviews/:id`: Update a review
    - `DELETE /api/v1/reviews/:id`: Delete a review

 
