# Getting Started

This document helps you authenticate and make your first API request to retrieve or create user data.

## Authentication

If your API requires authentication, you will need to include an Authorization header in your requests. For example:

```yaml
Authorization: Bearer YOUR_API_TOKEN
```
Replace `YOUR_API_TOKEN` with your actual token.

## Make your first API request
### Retrieve all users
Use `GET /v1/users` to retrieve a list of all users, including each user's ID, name, and email address.

### Create a new user
Use `POST /v1/users` to add a new user.
To create a new user, follow the User schema, including all required fields such as ID, name and email address.
You will receive a confirmation when the user was successfully added.
