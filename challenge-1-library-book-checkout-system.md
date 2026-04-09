# Challenge 1 – Library Book Checkout System

## Challenge Overview

Build a comprehensive library management system that enables multiple user roles to manage book inventory and lending operations. The system should handle user registration, book cataloging, real-time availability tracking, and checkout/return workflows.

### Key Requirements

- **Admin functionality** for managing users and book inventory
- **User functionality** for discovering and checking out books
- **Real-time tracking** of book availability and checkout history
- **Business logic** to enforce lending rules and prevent conflicts
- **Persistent storage** for all data

---

## Problem Domain Breakdown

### 1. User Management
- Support different user roles (Admin, Librarian, Member)
- User registration and profile management
- Track user checkout history and outstanding items

### 2. Book Catalog
- Maintain a comprehensive book database with metadata (title, author, ISBN, etc.)
- Support multiple copies of the same book with unique identifiers
- Enable filtering and search by title, author, category, or ISBN

### 3. Checkout/Return Operations
- Implement checkout workflow with availability checks
- Manage return operations with late fee calculation
- Prevent double-checkout and handle edge cases

### 4. Data Persistence
- Store user, book, and transaction data persistently
- Maintain transaction history for audit and reporting
- Ensure data integrity across concurrent operations

### 5. Business Rules
- Enforce maximum books per user limit
- Calculate and track overdue items (books out >14 days)
- Generate reports on inventory status and member activity

---

## Core Entities & Relationships

```
User (id, name, email, role, joinDate)
  ├── Member (maxBooks: 5, currentBooks: [])
  └── Admin/Librarian (permissions)

Book (id, title, author, isbn, category, copies[])
  └── BookCopy (copyId, status, checkedOutBy, checkedOutDate, dueDate)

Checkout (id, userId, bookCopyId, checkoutDate, dueDate, returnDate)
```

---

## Prerequisites

- Strong understanding of object-oriented programming concepts
- Familiarity with relational databases and SQL
- Knowledge of REST API design principles
- **GitHub Copilot** - Must be enabled and configured for AI-assisted code generation and development support

---

## Example Prompts for Instructions & Agents

### Prompts for Instructions File

Use these prompts with GitHub Copilot to generate step-by-step implementation guides:

**Prompt 1 - Project Setup:**
```
Create a step-by-step guide for setting up a [Python/Java/Node.js] project structure for a Library Management System. 
Include folders for models, services, controllers, utilities, and tests. Add initialization and configuration steps.
```

**Prompt 2 - Database Schema:**
```
Design the database schema for a library system with User, Book, BookCopy, and Checkout tables. 
Include all fields, constraints, relationships, and indexes. Provide SQL DDL statements.
```

**Prompt 3 - Implementation Guide:**
```
Write a detailed implementation guide for building a REST API for [specific entity like User Management or Book Checkout].
Include code examples, error handling, and best practices for validation.
```

### Prompts for Creating Agents

Use these prompts to define custom agents for library-specific tasks:

**Agent 1 - Domain Logic Specialist:**
```
Create an agent that specializes in library domain logic. This agent should:
- Understand checkout rules (max books per user, 14-day limit, late fees)
- Generate code for validating business rules
- Ensure data integrity in transactions
- Provide domain-specific error messages
```

**Agent 2 - API Development Expert:**
```
Create an agent for REST API development that:
- Generates proper HTTP methods and status codes
- Implements error handling with meaningful messages
- Creates request/response DTOs with validation
- Adds proper logging and tracing
```

**Agent 3 - Test Generator:**
```
Create an agent that generates comprehensive test cases for:
- Happy path scenarios
- Edge cases (empty inventory, max books reached)
- Error scenarios (duplicate checkout, overdue items)
- Integration tests with database
```

---

## Core Features to Implement

### 1. User Management API
- User registration and authentication
- Role-based access control (Admin, Member)
- User profile and checkout history endpoints

### 2. Book Management API
- Add/update/delete books from catalog
- Track multiple copies per book
- Search and filter (title, author, category, ISBN, availability)

### 3. Checkout Operations API
- **Checkout**: Check availability → Reserve → Update status
- **Return**: Validate return → Calculate late fees → Update status
- **List**: Available books, user's checked-out books, overdue items

### 4. Reporting & Analytics
- Inventory status reports
- Member activity reports
- Overdue notifications
- Popular books statistics

---

## Tech Stack Options

Choose your preferred technology combination:

### Option 1: Python
**Backend**: Django/FastAPI | **Database**: SQLite/PostgreSQL | **Testing**: pytest | **Frontend**: React/Vue/Flask templates

### Option 2: Java
**Backend**: Spring Boot | **Database**: H2/PostgreSQL | **Testing**: JUnit5 + Mockito | **Frontend**: React/Thymeleaf

### Option 3: Node.js
**Backend**: Express/NestJS | **Database**: MongoDB/PostgreSQL | **Testing**: Jest | **Frontend**: React/Vue/EJS

### Option 4: Other
Use any language/framework of your choice - focus on the functionality, not the stack.

---

## Development Workflow Phases

**⚠️ Important**: You must use **GitHub Copilot** throughout this challenge for code generation, testing, and documentation. It will accelerate development and help you follow best practices.

Follow these phases in order for successful completion:

1. **Requirement Document** - Define functional and non-functional requirements for the library system
2. **Plan** - Design database schema, API architecture, and component interactions
3. **Instructions** - Write implementation guide for your chosen tech stack
4. **Prompts** - Define prompts to assist with code generation
5. **Chat Participants and Variables** - Set up collaboration context and variables
6. **Agents** - Configure any custom agents for your domain
7. **Custom Agent** - Create specialized agent for library-specific business logic
8. **Generating Code Using Agent/Custom Agent** - Generate project scaffold and initial code
9. **API Generation** - Implement REST endpoints for all entities and operations
10. **UI Generation** - Build user interfaces for member and admin workflows
11. **Unit Test Cases** - Write unit tests for business logic and edge cases
12. **Automation Testing** - Implement integration and end-to-end tests
13. **Documentation** - Create API docs, user guides, and technical documentation

---

## Expected Deliverables

- ✅ **Source Code** in `/src` folder (organized by layers: model, service, controller, util)
- ✅ **Test Suite** with unit and integration tests (min 70% coverage)
- ✅ **API Documentation** in `/docs/API.md` (endpoints, request/response schemas)
- ✅ **User Guide** in `/docs/USER_GUIDE.md` (workflows, features)
- ✅ **Technical Documentation** in `/docs/TECHNICAL.md` (architecture, database schema)
- ✅ **Database Schema** in `/docs/DATABASE_SCHEMA.md`
- ✅ **Sample Data** in `/data/sample.json` or equivalent

---

## Validation Criteria

Your solution will be validated against:

- ✅ **App Must Be Running** - Application starts without errors, all endpoints accessible
- ✅ **Tests Must Be Passing** - 100% of unit and integration tests pass with >70% code coverage
- ✅ **Exceptions/Errors Must Be Handled** - Graceful error handling with meaningful messages for invalid operations
- ✅ **Documents Must Be Present in /docs Folder** - Complete API docs, user guide, and technical documentation
- ✅ **Source Code Must Be Present in /src Folder** - Well-organized, readable code with proper structure

---

## Challenge Extension Ideas (If Time Permits)

- Implement reservation system for unavailable books
- Add email notifications for due dates and availability
- Create admin dashboard with analytics
- Implement fine/penalty system with payment tracking
- Add book recommendations based on checkout history
- Support book requests and waitlist functionality

---

**END OF CHALLENGE 1**