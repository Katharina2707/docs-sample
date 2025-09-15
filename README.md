# User API

Welcome to the **User API** repository. This project provides a RESTful interface for managing user data, built using the OpenAPI 3.0 specification.

The API allows you to:
- **List all users** (`GET /v1/users`)
- **Create a new user** (`POST /v1/users`)

It returns and accepts data in JSON format and follows standard HTTP response codes.

## Getting Started

To learn how to authenticate and make your first API request, see the **Getting Started Guide**.

## Endpoints

To learn about the endpoints and the components, see the **Users Guide**.

### `GET /v1/users`
- **Summary**: Retrieve a list of all users.
- **Response**: `200 OK` with a JSON array of user objects.

### `POST /v1/users`
- **Summary**: Create a new user.
- **Request Body**: JSON object matching the `User` schema.
- **Response**: `201 Created` when the user is successfully added.

## 🧩 Components

### `User` Schema
```yaml
type: object
properties:
  id:
    type: string
  name:
    type: string
  email:
    type: string  # Note: description missing


