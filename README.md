# 📚 Library Management System

This project is a console-based Library Management System written in C, designed to demonstrate core procedural programming concepts along with modular design and unit testing.

### Core Features

| Category | Role | Feature |
| :--- | :--- | :--- |
| **System Interface** | Shared | Menu-driven terminal application |
| **Book Management** | Librarian | Add book, Remove book, View all available books |
| **Issue Management** | Issue | Issue book to student, View issued book list |
| **Data Storage** | Persistence | Binary files (`books.txt`, `issue.txt`) for records |
| **Quality Assurance** | Testing | Dedicated unit-style tests for validation logic |

### File Map

| Module | File | Purpose |
| :--- | :--- | :--- |
| **System Core** | `main.c` | Handles the main menu, navigation, and program flow. |
| **Book Operations** | `books.c` | Logic for adding books (`addBook`), includes `isValidBookId`. |
| **List/View** | `list.c` | Logic for viewing books (`booksList`), includes `isValidListCount`. |
| **Deletion** | `delete.c` | Logic for removing books (`del`), includes `isValidDeleteId`. |
| **Issue Records** | `issue.c` | Logic for issuing books (`issueBook`, `issueList`), includes `isValidIssueId`. |
| **Validation Tests** | `test_*.c` | Individual test files for all validation functions. |

### Build & Run

**Requirements:** GCC (MinGW on Windows, or standard GCC on Linux/macOS)

```bash
# 1. Compile main application
gcc ./main.c

# 2. Run
./a.exe
# --- Running Unit Tests (Example: Testing Book Validation) ---

# Unit test (example)
gcc test_books.c -DUNIT_TEST
# Run
./a.exe
# Expected Output: All tests should report 'success: 1'.
```