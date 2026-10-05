# API Test Report
Tool: Postman

## Test Case 1: Borrow Book (Normal)
- Method: POST
- Endpoint: /api/borrow
- Request: {"bookId":1,"readerId":1}
- Expected: 200 OK, create borrow record, reduce available quantity.

## Test Case 2: Borrow Book (No stock)
- Method: POST
- Endpoint: /api/borrow
- Request: {"bookId":2,"readerId":1}
- Expected: 400 Bad Request, message: No available copies for this book.

## Test Case 3: Return Book (Normal)
- Method: POST
- Endpoint: /api/return
- Request: {"recordId":1}
- Expected: 200 OK, fill return date, increase book quantity.

## Test Case 4: Return invalid record
- Method: POST
- Endpoint: /api/return
- Request: {"recordId":999}
- Expected: 404 Not Found, message: Borrow record does not exist.

## Test Case 5: Return book twice
- Method: POST
- Endpoint: /api/return
- Request: {"recordId":1}
- Expected: 400 Bad Request, message: This book has already been returned.

