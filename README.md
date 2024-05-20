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

# University Library REST API

## Authentication
- **POST /api/auth/login:** Login with username and password.
- **POST /api/auth/logout:** Logout the currently logged-in user.
- **POST /api/auth/register:** Register a new user with username, email, and password.

## Books
- **GET /api/books:** Retrieve a list of all books.
- **GET /api/books/{id}:** Get details of a specific book by ID.
- **POST /api/books:** Add a new book to the library.
- **PUT /api/books/{id}:** Update information for a specific book by ID.
- **DELETE /api/books/{id}:** Delete a book from the library by ID.

## Authors
- **GET /api/authors:** Get a list of all authors.
- **GET /api/authors/{id}:** Get details of a specific author by ID.
- **POST /api/authors:** Add a new author to the system.
- **PUT /api/authors/{id}:** Update information for a specific author by ID.
- **DELETE /api/authors/{id}:** Remove an author from the system by ID.

## Users
- **GET /api/users:** Retrieve a list of all users (admin access).
- **GET /api/users/{id}:** Get details of a specific user by ID (admin access).
- **PUT /api/users/{id}:** Update user information by ID (admin access).
- **DELETE /api/users/{id}:** Delete a user from the system by ID (admin access).

## Loans
- **GET /api/loans:** Retrieve a list of all active loans.
- **GET /api/loans/{id}:** Get details of a specific loan by ID.
- **POST /api/loans:** Create a new loan for a user.
- **PUT /api/loans/{id}:** Update loan information (e.g., return date) by ID.
- **DELETE /api/loans/{id}:** Cancel a loan by ID.

## Departments
- **GET /api/departments:** Get a list of all departments.
- **GET /api/departments/{id}:** Get details of a specific department by ID.
- **POST /api/departments:** Add a new department to the library.
- **PUT /api/departments/{id}:** Update department information by ID.
- **DELETE /api/departments/{id}:** Remove a department from the system by ID.

## Notifications
- **GET /api/notifications:** Get a list of notifications for the current user.
- **POST /api/notifications:** Send a new notification to a user.

## Reports
- **GET /api/reports/loans:** Generate a report of all book loans.
- **GET /api/reports/overdue:** Generate a report of overdue books.
- **GET /api/reports/popular-books:** Get a list of popular books based on loan history.

## Analytics
- **GET /api/analytics/usage:** Get usage analytics for the library system.
- **GET /api/analytics/traffic:** Get traffic analytics for the library website.

