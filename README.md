# Registration Form

This repository contains a registration form page and its related project files.

## Overview

The registration form page is intended to collect user registration details through a simple interface.
This README is provided to give users and contributors a clear starting point when opening the repository.

## Contents

- Registration form page source files
- Supporting project assets and configuration

## Notes

Update this README with project-specific setup, usage, and deployment instructions as the repository evolves.

## API Documentation

The registration form is designed to submit user details to a registration API.

### Register User

- **Method:** `POST`
- **Path:** `/api/register`
- **Content-Type:** `application/json`

#### Request Body

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | Yes | Full name of the user. |
| `email` | string | Yes | User email address. |
| `password` | string | Yes | User account password. |

#### Successful Response

- **Status:** `201 Created`
- **Body:**

```json
{
  "message": "User registered successfully",
  "userId": "abc123"
}
```

#### Error Responses

- `400 Bad Request` — Missing or invalid input fields.
- `409 Conflict` — Email already registered.
- `500 Internal Server Error` — Unexpected server error.
