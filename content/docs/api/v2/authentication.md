# Authentication API (v2)

This document describes the endpoints and usage for the v2 Authentication API.

## Endpoints

### `POST /api/v2/auth/login`

Authenticate a user and receive a JWT token.

**Request Body:**
```json
{
    "username": "string",
    "password": "string"
}
```

**Response:**
```json
{
    "token": "jwt-token-string"
}
```

### `POST /api/v2/auth/logout`

Invalidate the current user's session.

**Headers:**
- `Authorization: Bearer <token>`

**Response:**
```json
{
    "success": true
}
```

### `POST /api/v2/auth/refresh`

Refresh the JWT token.

**Headers:**
- `Authorization: Bearer <token>`

**Response:**
```json
{
    "token": "new-jwt-token-string"
}
```

## Error Handling

All error responses follow this format:

```json
{
    "error": "Error message"
}
```

## Notes

- All endpoints require HTTPS.
- Tokens expire after 1 hour by default.
- Use the refresh endpoint to obtain a new token before expiration.
