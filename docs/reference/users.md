# User API Reference

**Version**: 1.0.0 

The User API allows you to list, create, and manage users. It follows RESTful principles and returns JSON-formatted responses.

## Endpoints

### `GET /v1/users`
- Description: Retrieve a list of all users.
- Method: `GET`
- Response: `200 OK` – Returns an array of user objects.
- Example curl request:
```yaml
curl -X GET https://your-api-domain.com/v1/users
```
- Response Schema:
```yaml
[
  {
    "id": "string",
    "name": "string",
    "email": "string"
  }
]
```

### `POST /v1/users`
- Description: Create a new user.
- Method: `POST`
- Request Body:
```yaml
{
  "id": "string",
  "name": "string",
  "email": "string"
}
```
- Response: `201 Created` – Returns the created user object.
- Example curl request:
```yaml
curl -X POST https://your-api-domain.com/v1/users \
  -H "Content-Type: application/json" \
  -d '{
    "id": "123",
    "name": "Jane Doe",
    "email": "jane@example.com"
  }'
```

## User schema
```yaml
type: object
properties:
  id:
    type: string
    description: Unique identifier for the user   #Suggestion to add a description
  name:
    type: string
    description: Full name of the user            #Suggestion to add a description
  email:                                          #Suggestion to add email
    type: string
    format: email                                 #Suggestion to add format to indicates that the string should follow a valid email format
    description: email address of the user
```

## Authentication
```yaml
-H " X-API-Key: publicprefix.secret"

