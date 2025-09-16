# User API quick start
This API allows you to manage users.

## Retrieve all users
To retrieve a list of users, use the following command:
```yaml
curl -X GET https://api.example.com/v1/users
```
You will receive a list of users.

## Create a user

To create a user, use the following command:
```yaml
curl -X POST https://api.example.com/v1/users \
     -H "Content-Type: application/json" \
     -d '{
      "id": "12345",
      "name": "John",
      "email": "john@example.com"
      }'

```
You will receive a JSON object representing the newly created user.

