# Borrow & Return Business Logic Design
## Borrow Book Logic
1. Check if target book has available copies.
2. If available: create new BorrowRecord, reduce book available quantity.
3. If no available books: reject borrow request and return error message.

## Return Book Logic
1. Search borrow record by record id.
2. If record exists and not returned: fill return date, increase book available quantity.
3. If record invalid or already returned: reject return request.

## Edge Cases
- Borrow book with quantity = 0
- Return non-existing borrow record
- Return book that already returned
