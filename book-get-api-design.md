# Book GET API Design
## Endpoint 1: Get all books
GET /api/books
Response 200 OK
[
  {
    "bookId":1,
    "title":"The Great Gatsby",
    "author":"F. Scott Fitzgerald",
    "availableQuantity":3
  }
]

## Endpoint 2: Get single book by id
GET /api/books/{id}
Response 200 OK
{
  "bookId":1,
  "title":"The Great Gatsby",
  "author":"F. Scott Fitzgerald",
  "availableQuantity":3
}

### Error Response
Status code: 404 Not Found
```json
{
  "message": "The book with this ID cannot be found."
}
