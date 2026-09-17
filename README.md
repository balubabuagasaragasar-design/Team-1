📚 Library Management System

📌 Project Overview

The Library Management System is a simple database-based project designed to manage students, books, book issues, and book returns efficiently.

The system keeps track of student details, book information, issue dates, due dates, and return dates. It also checks whether a book is returned on or before the due date.

---

🎯 Objectives

- Store and manage student information.
- Store and manage book information.
- Check book availability before issuing.
- Record book issue details.
- Set and store the due date.
- Record book return details.
- Check the return date against the due date.
- Maintain updated book availability.
- Display transaction details clearly.

---

🗂️ Main Modules

1. Student Details

Stores information about library students:

- Student ID
- Student Name
- Class
- Contact Number

2. Book Details

Stores information about available books:

- Book ID
- Book Name
- Author
- Quantity

3. Book Issue

Records the issue of a book:

- Student ID
- Book ID
- Issue Date
- Due Date

4. Book Return

Records the return of a book:

- Student ID
- Book ID
- Return Date
- Due Date Check

The system compares the Return Date with the Due Date to determine whether the book was returned on time.

---

🔄 System Flow

START
  ↓
Enter Student Details
  ↓
Enter Book Details
  ↓
Check Book Availability
  ↓
Is Book Available?
  ├── No → Display "Book Not Available" → END
  ↓ Yes
Issue Book
  ↓
Set Due Date
  ↓
Return Book
  ↓
Check Return Date with Due Date
  ↓
Update Book Availability
  ↓
Display Transaction Details
  ↓
END

---

🧮 Algorithm

1. Start.
2. Enter and store student details.
3. Enter and store book details.
4. Check whether the requested book is available.
5. If the book is available, issue the book and record the issue date.
6. Calculate and store the due date.
7. When the student returns the book, record the return date.
8. Compare the return date with the due date.
9. Update the book availability.
10. Display the transaction details.
11. Stop.

---

🗃️ ER Diagram Structure

The system contains three main entities:

STUDENT

Attribute| Description
Student_ID| Primary Key
Student_Name| Student's name
Class| Student's class
Contact_No| Contact number

BOOK

Attribute| Description
Book_ID| Primary Key
Book_Name| Name of the book
Author| Book author
Quantity| Number of available books

ISSUE_RETURN

Attribute| Description
Transaction_ID| Primary Key
Student_ID| Foreign Key
Book_ID| Foreign Key
Issue_Date| Date of issue
Due_Date| Expected return date
Return_Date| Actual return date

---

🔗 Relationships

- One STUDENT can have many book transactions.
- One BOOK can have many transactions over time.
- ISSUE_RETURN connects STUDENT and BOOK.
- "Student_ID" in ISSUE_RETURN references STUDENT.
- "Book_ID" in ISSUE_RETURN references BOOK.

STUDENT                    BOOK
   │                         │
   │                         │
   └────── ISSUE_RETURN ─────┘

---

🔑 Keys Used

Primary Keys

- "Student_ID" → STUDENT
- "Book_ID" → BOOK
- "Transaction_ID" → ISSUE_RETURN

Foreign Keys

- "Student_ID" → ISSUE_RETURN
- "Book_ID" → ISSUE_RETURN

---

🛠️ Flowchart Symbols

Symbol| Meaning
Oval| Start / End
Rectangle| Process
Diamond| Decision
Parallelogram| Input / Output

---

✅ Expected Outcome

The Library Management System provides an organized way to:

- Manage students.
- Manage books.
- Issue books.
- Track due dates.
- Record returned books.
- Check whether books are returned on time.
- Update book availability.
- Maintain transaction records.

---

📁 Project Structure

Library-Management-System/
│
├── README.md
├── Flowchart
├── Algorithm
├── ER-Diagram
└── Database

---

👨‍💻 Conclusion

The Library Management System simplifies basic library operations by connecting student records, book records, and issue/return transactions. It provides a clear and systematic method for maintaining library information.
