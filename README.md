# BookCase

This is a part of an exercise for a [Full Stack Development Challenge](https://github.com/infoxchange/full-stack-developer-challenge).
This implementation is purely for educational and experimental purpose. 


This is a small web application for managing a list of books.
Each book will have an **ISBN**, **name** and **author**.
Each author will be having a **first name** and **last name**.

### Backend Implementation

Use the following structure to model the data:

```python3
class Author(Model):
    first_name = models.TextField()
    last_name = models.TextField()
```

```python3
class Book(Model):
    name = models.TextField()
    isbn = models.TextField()
    author = models.ForeignKey(Author)
```

Implement the following API endpoints:

- **GET /books/** - Returns a list of books in the database in JSON format
- **GET /book/{{id}}/** - Returns a detail view of the specified book id. Nest author details in JSON format
- **GET /authors/** - Returns a list of authors in the database in JSON format
- **GET /author/{{id}}/** - Returns a detail view of the specified author id
- **POST /author/*** - Creates a new author with the specified details - Expects a JSON body
- **POST /book/** - Creates a new book with the specified details - Expects a JSON body
- **PUT /author/{{id}}** - Updates an existing author - Expects a JSON body
- **PUT /book/{{id}}** - Updates an existing book - Expects a JSON body

For backend we are going to use the below technologies:
- Postgres DB
- Golang/Gin
- REST API
- OAuth2.0 (Google SignIn)


### Frontend Implementation

No design is given, so I am going to use my judgement to the best of my knowledge
and the obvious choice in **2025** is ReactJs!


