# Book POST API Design
## Endpoint: Add new book
POST /api/books

## Request Body
```json
{
  "title": "The Great Gatsby",
  "author": "F. Scott Fitzgerald",
  "availableQuantity": 3
}

{
  "bookId": 1,
  "title": "The Great Gatsby",
  "author": "F. Scott Fitzgerald",
  "availableQuantity": 3
}

{
  "message": "Title and author are required."
}
