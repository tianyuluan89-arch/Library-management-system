# UML Class Diagram - Library Management System
This document describes the core classes, attributes, methods and relationships for the library management system.

## 1. Book Class
| Attribute | Type | Visibility |
| ---- | ---- | ---- |
| bookId | int | private |
| title | string | private |
| author | string | private |
| availableQuantity | int | private |

Methods:
- GetBookInfo(): return book details
- ReduceQuantity(): decrease available quantity when borrowing
- IncreaseQuantity(): increase available quantity when returning

## 2. Reader Class
| Attribute | Type | Visibility |
| ---- | ---- | ---- |
| readerId | int | private |
| fullName | string | private |
| contact | string | private |
| registerDate | Date | private |

Methods:
- GetReaderInfo(): return reader information

## 3. BorrowRecord Class
| Attribute | Type | Visibility |
| ---- | ---- | ---- |
| recordId | int | private |
| bookId | int | private |
| readerId | int | private |
| borrowDate | Date | private |
| returnDate | Date | private |

Methods:
- CreateRecord(): create new borrowing record
- FinishReturn(): fill return date and complete borrowing process

## Class Relationships
1. One Book can have many BorrowRecord (1 to *)
2. One Reader can have many BorrowRecord (1 to *)
3. BorrowRecord acts as the linking class between Book and Reader.
