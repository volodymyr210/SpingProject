### Functional Requirements

#### User Authentication
- Users should be able to register, login, and logout from the system.
- Users must have different roles such as students, staff, and administrators.

#### Book Search and Reservation
- Users should be able to search for books by title, author, or ISBN.
- Users can view book availability and reserve books if they are available.

#### Loan Management
- The system should allow users to borrow books and specify the loan duration.
- Overdue notifications should be sent to users who fail to return books on time.

#### Profile Management
- Users should be able to update their profiles, including contact information and password changes.
- Staff members and administrators should have additional functionalities for managing user profiles.

#### Department Management
- Staff members should be able to add, edit, and delete departments in the library system.
- Each department should have a designated quantity of books available.

#### Author Information
- Users should be able to access information about authors, including their nationality and birthdate.
- The system should display a list of books written by each author.

#### Book Inventory Management
- Staff members should have privileges to add new books to the inventory with details such as title, ISBN, publisher, and year published.
- The system should track the quantity of each book available in the library.

#### Email Notifications
- Users should receive email notifications for actions such as book reservations, loan due dates, and overdue fines.
- The system should send reminders for overdue books and fines.

#### Reports and Analytics
- Administrators should have access to generate reports on book loans, overdue books, popular books, and user activities.
- The system should provide analytics to help improve library services and resource management.

#### Accessibility and Security
- The system should be accessible to users with disabilities, following accessibility standards.
- Data security measures such as encryption and regular backups should be implemented to protect user information and library data.\

### System Behaviors

#### User Authentication
- Users can register by providing required information such as name, email, and password.
- Upon successful registration, users receive a confirmation email.
- Users can log in using their email and password.
- Forgot password functionality allows users to reset their passwords via email verification.
- Users can log out from the system at any time.

#### Book Search and Reservation
- The search functionality allows users to search for books by title, author, or ISBN.
- Search results display book details and availability status.
- Users can reserve books if they are available by selecting the desired quantity.
- Reserved books are marked as unavailable for other users until the reservation expires.

#### Loan Management
- Users can borrow books by selecting them from the available inventory.
- The system calculates and displays the loan duration based on user preferences.
- Overdue notifications are sent to users via email if they fail to return books on time.
- Users can extend the loan duration if allowed by the system.

#### Profile Management
- Users can update their profiles, including personal information, contact details, and password changes.
- Staff members and administrators have additional options to manage user profiles, such as editing roles and permissions.

#### Department Management
- Staff members can add new departments to the library system.
- Editing options allow staff members to update department details and book quantities.
- Deleting a department removes all associated books and user data from the system.

#### Author Information
- Users can view detailed information about authors, including their nationality, birthdate, and a list of books they have authored.
- The system displays author profiles with relevant information and links to their published works.

#### Book Inventory Management
- Staff members have access to add new books to the inventory, including details such as title, ISBN, publisher, and year published.
- Editing options allow staff members to update book information and quantities.
- The system tracks book availability and updates inventory status in real-time.

#### Email Notifications
- Email notifications are sent to users for actions such as account registration, password reset, book reservations, loan due dates, and overdue fines.
- Reminders are sent for upcoming due dates and overdue books to prompt users to return borrowed items.

#### Reports and Analytics
- Administrators can generate reports on various aspects of the library system, including book loans, overdue books, popular books, and user activities.
- Analytics tools provide insights into user behavior, resource utilization, and system performance to support decision-making and improvements.

#### Accessibility and Security
- The system complies with accessibility standards to ensure usability for users with disabilities, including screen reader compatibility and keyboard navigation.
- Data security measures such as encryption, secure login, role-based access control, and regular data backups are implemented to protect user information and library data.

# REST API for University Library Management

## Books Endpoint

### GET /books
- Description: Get a list of all books in the library.
- Response: JSON array of book objects.

### GET /books/{book_id}
- Description: Get details of a specific book by its ID.
- Response: JSON object with book details.

### POST /books
- Description: Add a new book to the library.
- Request Body: JSON object with book details (title, ISBN, publisher, year_published).
- Response: Success message with the ID of the newly added book.

### PUT /books/{book_id}
- Description: Update details of a specific book.
- Request Body: JSON object with updated book details.
- Response: Success message.

### DELETE /books/{book_id}
- Description: Delete a book from the library by its ID.
- Response: Success message.

## Authors Endpoint

### GET /authors
- Description: Get a list of all authors in the library.
- Response: JSON array of author objects.

### GET /authors/{author_id}
- Description: Get details of a specific author by their ID.
- Response: JSON object with author details.

### POST /authors
- Description: Add a new author to the library.
- Request Body: JSON object with author details (name, nationality, birthdate).
- Response: Success message with the ID of the newly added author.

### PUT /authors/{author_id}
- Description: Update details of a specific author.
- Request Body: JSON object with updated author details.
- Response: Success message.

### DELETE /authors/{author_id}
- Description: Delete an author from the library by their ID.
- Response: Success message.

## Loans Endpoint

### GET /loans
- Description: Get a list of all active loans in the library.
- Response: JSON array of loan objects.

### GET /loans/{loan_id}
- Description: Get details of a specific loan by its ID.
- Response: JSON object with loan details.

### POST /loans
- Description: Create a new loan for a book.
- Request Body: JSON object with loan details (book_id, borrower_id, loan_date, return_date).
- Response: Success message with the ID of the newly created loan.

### PUT /loans/{loan_id}
- Description: Update details of a specific loan.
- Request Body: JSON object with updated loan details.
- Response: Success message.

### DELETE /loans/{loan_id}
- Description: Delete a loan from the library by its ID.
- Response: Success message.

## Users (Students/Staff) Endpoint

### GET /users
- Description: Get a list of all users (students/staff) in the library system.
- Response: JSON array of user objects.

### GET /users/{user_id}
- Description: Get details of a specific user by their ID.
- Response: JSON object with user details.

### POST /users
- Description: Register a new user (student or staff).
- Request Body: JSON object with user details (name, email, address, department, role).
- Response: Success message with the ID of the newly registered user.

### PUT /users/{user_id}
- Description: Update details of a specific user.
- Request Body: JSON object with updated user details.
- Response: Success message.

### DELETE /users/{user_id}
- Description: Delete a user from the library system by their ID.
- Response: Success message.


