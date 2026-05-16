# QA Report

## Bug: Whitespace-only title is allowed

### Summary
System allows creation of items where title contains only spaces.

### Endpoint
POST /api/v1/items/

### Payload
{
  "title": "     ",
  "description": "test"
}

### Actual Result
Item is created and stored in database.

### Expected Result
System should reject whitespace-only titles with validation error.

### Severity
Medium
