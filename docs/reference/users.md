# Users Guide

This document contains information for end users of the project.


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
