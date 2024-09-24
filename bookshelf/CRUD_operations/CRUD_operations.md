# CRUD Operations for Book Model

## 1. Create Operation

The following command creates a new `Book` instance with the title **1984**, author **George Orwell**, and publication year **1949**.

### Command:
```python
from bookshelf.models import Book
book = Book.objects.create(title="1984", author="George Orwell", publication_year=1949)

#### Output:
<Book: 1984 by George Orwell>


## 2. Retrieve Operation

This command retrieves the book you created earlier.

### Command:
book = Book.objects.get(id=1)
print(book.title, book.author, book.publication_year)

##### Output:
1984 George Orwell 1949

## 3. Update Operation

Here, we update the book's title from 1984 to Nineteen Eighty-Four.

### Command:
book.title = "Nineteen Eighty-Four"
book.save()

##### Output:
<Nineteen Eighty-Four by George Orwell>

## 4. Delete Operation

Finally, this command deletes the book instance and confirms its deletion by trying to retrieve all books again.

### Command:
book.delete()
books = Book.objects.all()
print(books)

##### Output:
[]



















