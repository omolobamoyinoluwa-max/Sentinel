# Endpoint Name

## Overview

Brief description of the endpoint.

## Endpoint

```http
METHOD /api/resource
```

## Authentication

Required | Optional | None

## Request

### Headers

| Header        | Required | Description  |
| ------------- | -------- | ------------ |
| Authorization | Yes      | Bearer token |

### Query Parameters

| Parameter | Type   | Required | Description |
| --------- | ------ | -------- | ----------- |
| page      | number | No       | Page number |

### Request Body

```json
{
  "example": "value"
}
```

## Success Response

**Status:** `200 OK`

```json
{
  "success": true,
  "data": {}
}
```

## Error Responses

### 400 Bad Request

```json
{
  "success": false,
  "error": "Validation failed"
}
```

### 404 Not Found

```json
{
  "success": false,
  "error": "Resource not found"
}
```

## Notes

Additional implementation details.

# API Error Reference

## Standard Error Format

```json
{
  "success": false,
  "error": "Error description"
}
```

## Common Status Codes

| Status | Description           |
| ------ | --------------------- |
| 200    | Success               |
| 201    | Resource created      |
| 400    | Bad request           |
| 401    | Unauthorized          |
| 403    | Forbidden             |
| 404    | Not found             |
| 409    | Conflict              |
| 422    | Validation error      |
| 500    | Internal server error |

## Example Validation Error

```json
{
  "success": false,
  "error": "Email format is invalid"
}
```
