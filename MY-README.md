# Project Description

This project is a fork from [krishnaacharyaa](https://github.com/krishnaacharyaa). It includes a full-stack application with a React frontend, Node.js backend, and MongoDB as the database. To streamline the development and deployment process, I have created Dockerfiles for both the frontend and backend, as well as a `docker-compose.yml` file to manage the entire application.

## Project Structure

- **Backend**: Node.js application
- **Frontend**: React application with Vite
- **Database**: MongoDB

## Docker Setup

### Backend Dockerfile

The backend Dockerfile sets up a Node.js environment, installs dependencies, and starts the application on port 5000.

### Frontend Dockerfile

The frontend Dockerfile configures a React development server using Vite, installs necessary dependencies, and starts the frontend on port 5173.

### Docker Compose Configuration

The `docker-compose.yml` file manages and orchestrates the services for the application:

- **MongoDB Service**: Uses the latest MongoDB image, maps the local data directory to the container, and exposes port 27017.
- **Frontend Service**: Builds the frontend from the specified Dockerfile, uses environment variables, maps local files to the container, and exposes port 5173.
- **Backend Service**: Builds the backend from the specified Dockerfile, uses environment variables, and exposes port 5000. It depends on the MongoDB service to be up and running.

This setup provides a cohesive environment for running and developing a 3-tier application using Docker and Docker Compose. The React frontend communicates with the Node.js backend, and the backend interacts with the MongoDB database.

