# Return Book API Design
## Endpoint
POST /api/return

## Request Body
```json
{
  "recordId": 1
}


Success  Response
{
  "recordId": 1,
  "bookId": 1,
  "readerId": 1,
  "borrowDate": "2026-10-05",
  "returnDate": "2026-10-05"
}

Error Response:404 Not Found
{
  "message": "Borrow record does not exist"
}


Status  code:400 Bad Resquest
{
  "message": "This book has already been returned"
}
