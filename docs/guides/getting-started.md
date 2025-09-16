# Getting Started with the User API

This document helps you authenticate and make your first API request to retrieve or create user data.

## Authentication

In order to be able to use the User API, you will need to authenticate yourself.
Create an API Key and provide a label for it, so that you can easily recognize it later.
Keep your API Key somewhere safe and do not share it with anyone.

To perform any API call, you will need to provide your API Key in an authentication header.
The format is the following:
```yaml
X-API-Key: publicprefix.secret
```

## Make your first API call

### Retrieve all users
Use `GET /v1/users` to retrieve a list of all users, including each user's ID, name, and email address. You will need to enter your API Key as well:
```yaml
curl -X GET https://your-api-domain.com/v1/users \
  -H " X-API-Key: publicprefix.secret"
```

### Create a new user
Use `POST /v1/users` to add a new user. To create a new user, follow the [User schema](../reference/users.md#User-schema), including all required fields such as ID, name and email address.
You will need to enter your API Key as well. For example:
```yaml
curl -X POST https://your-api-domain.com/v1/users \
  -H "Content-Type: application/json" \
  -H " X-API-Key: publicprefix.secret" \
  -d '{
    "id": "12345",
    "name": "Jane Doe",
    "email": "jane.doe@example.com"
  }'
```

You will receive a confirmation when the user was successfully added.
