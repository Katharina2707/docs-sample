# User API quick start
This API allows you to manage users.

## Get users
To retrieve a list of users, use the following command:

curl GET https://api.example.com/v1/users

Response: list of user objects

## Create a user

To create a user, use the following command:

curl -X POST https://api.example.com/v1/users \
     -H "Content-Type: application/json" \
     -d '{"name": "John", "email": "john@example.com"}'

Response:
A JSON object representing the newly created user.

