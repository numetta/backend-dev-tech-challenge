# Backend Developer Technical Challenge

## The Challenge

We're looking for a backend developer who can build robust, scalable APIs using modern Python practices. In this challenge, you'll develop a Book Management System that demonstrates your expertise in API development, database design, and software architecture.

The system will allow users to manage their reading lists and track reading progress, showcasing your ability to handle complex business logic while maintaining clean code and proper system design.

## Learning Objectives

- Implement a RESTful API using FastAPI
- Apply Domain-Driven Design principles
- Write comprehensive tests
- Use containerization
- Implement proper dependency management
- Follow Git best practices

## Requirements

### Required Technical Stack

- Python 3.11+
- FastAPI framework
- PostgreSQL database
- SQLAlchemy ORM
- Poetry for dependency management
- Docker and docker-compose
- pytest for testing
- Pre-commit hooks
- Conventional Commits for version control

### Core Features

The Book Management System should implement the following features:

1. Book Management:
   - Add new books (title, author, ISBN, publication year, genre)
   - Update book information
   - Delete books
   - List all books with pagination
   - Search books by title, author, or ISBN
2. Reading Lists:
   - Create reading lists
   - Add/remove books to/from reading lists
   - Track reading progress (not started, in progress, completed)
   - Add notes to books in reading lists
  
### Technical Requirements

#### API Design

- Follow RESTful principles
- Implement proper HTTP methods and status codes
- Follow FastAPI best practices
   - Use Pydantic models for request/response schemas
   - Implement proper dependency injection
   - Use proper error handling with HTTPException
   - Implement proper response models
- Implement proper separation of concerns using the CRUD pattern

#### Project Structure

```
├── app/
│   ├── api/
│   │   ├── v1/
│   │   │   ├── endpoints/
│   │   │   │   ├── books.py
│   │   │   │   └── reading_lists.py
│   │   │   └── api.py
│   ├── core/
│   │   ├── config.py
│   │   └── database.py
│   ├── crud/
│   │   ├── base.py
│   │   ├── crud_book.py
│   │   └── crud_reading_list.py
│   ├── models/
│   │   ├── book.py
│   │   └── reading_list.py
│   ├── schemas/
│   │   ├── book.py
│   │   └── reading_list.py
│   └── main.py
├── tests/
│   ├── api/
│   │   └── v1/
│   │       ├── test_books.py
│   │       └── test_reading_lists.py
│   └── crud/
│       ├── test_book.py
│       └── test_reading_list.py
├── docker/
│   ├── Dockerfile
│   └── docker-compose.yml
├── pyproject.toml
└── .pre-commit-config.yaml
```

#### Testing Requirements

- Implement unit tests for all services and repositories
- Implement integration tests for API endpoints
- Achieve minimum 80% test coverage
- Include tests for error cases and edge scenarios

#### Docker Setup

- Create a Dockerfile for the application
- Create a docker-compose.yml for local development
- Include PostgreSQL as the database
- Ensure proper environment variable handling

#### Poetry Configuration

- Set up proper dependency management
- Include development dependencies
- Configure virtual environment handling

#### Git and Commits

- Use Conventional Commits format
- Configure pre-commit hooks for:
  - Code formatting (black)
  - Import sorting (isort)
  - Linting (flake8)
  - Type checking (mypy)
  - Conventional commit message checking

### API Endpoints

#### Books

- `GET /api/v1/books` - List books (with pagination)
- `GET /api/v1/books/{book_id}` - Get book details
- `POST /api/v1/books` - Create new book
- `PUT /api/v1/books/{book_id}` - Update book
- `DELETE /api/v1/books/{book_id}` - Delete book
- `GET /api/v1/books/search` - Search books

#### Reading Lists

- `GET /api/v1/reading-lists` - List user's reading lists
- `POST /api/v1/reading-lists` - Create new reading list
- `GET /api/v1/reading-lists/{list_id}` - Get reading list details
- `PUT /api/v1/reading-lists/{list_id}` - Update reading list
- `DELETE /api/v1/reading-lists/{list_id}` - Delete reading list
- `POST /api/v1/reading-lists/{list_id}/books` - Add book to reading list
- `DELETE /api/v1/reading-lists/{list_id}/books/{book_id}` - Remove book from reading list
- `PUT /api/v1/reading-lists/{list_id}/books/{book_id}/progress` - Update reading progress

### Evaluation Criteria

#### Code Quality

- Clean, readable, and well-documented code
- Comprehensive error handling
- Proper use of type hints
- Adherence to PEP 8 standards
- Implementation of SOLID principles

#### Architecture

- Domain-driven design implementation
- Effective use of FastAPI features
- PostgreSQL database design and optimization
- RESTful API design
- Proper dependency injection
- Clear separation of concerns

#### Testing

- Comprehensive test coverage
- Well-organized test suite
- Edge case handling
- Integration tests
- Database interaction tests

#### DevOps and Tools

- Docker and docker-compose configuration
- Poetry dependency management
- Git workflow and commit quality
- Pre-commit hooks setup
- Environment configuration

#### Documentation

- API documentation (Swagger/OpenAPI)
- Setup and deployment instructions
- Code documentation
- README completeness
- API usage examples

### Deliverables

1. Complete implementation of the required features
2. Comprehensive test suite with good coverage
3. Docker and docker-compose setup for easy deployment
4. Poetry configuration for dependency management
5. Pre-commit hooks configuration
6. Clear documentation of your API endpoints

Focus on writing clean, maintainable code that follows FastAPI best practices.

### Time Expectation

You have 48 hours to complete this challenge from the moment you receive access to the repository. While we understand this is a tight timeline, we want to see how you handle time constraints while maintaining code quality.

### Bonus Points

- Implement API authentication
- Add API rate limiting
- Include Swagger documentation
- Add CI/CD pipeline
- Implement caching
- Add API versioning strategy
