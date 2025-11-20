

---

# 📘 Library Management System – SQL Project

## 📖 Overview

This project contains a complete SQL-based **Library Management System**.
The provided `.sql` file creates all required tables, relationships, and constraints for managing:

* Books & publishers
* Authors
* Library branches
* Borrowers
* Book copies
* Book loans

This project is suitable for learning SQL, practicing joins, and demonstrating a normalized relational database.

---

## 🏛 Database Structure (Summary)

### **1. Publishers (`tbl_publisher`)**

Stores publisher details (name, address, phone).

### **2. Books (`tbl_book`)**

Book information including title and publisher.

### **3. Book Authors (`tbl_book_authors`)**

Links each book to one or more authors.

### **4. Library Branches (`tbl_library_branch`)**

Branch name and location details.

### **5. Borrowers (`tbl_borrower`)**

Library user information.

### **6. Book Copies (`tbl_book_copies`)**

Tracks how many copies of each book exist in each branch.

### **7. Book Loans (`tbl_book_loans`)**

Records when borrowers check out and return books.

---

## ⚙️ How to Use

1. Open MySQL Workbench, phpMyAdmin, or any SQL client.
2. Import and run the SQL file:
   **`/mnt/data/206f360a-0a5a-491b-a909-7a744eca5636.sql`**
3. The database and tables will be created automatically.

---

## 📝 Example Queries

### Get books by author

```sql
SELECT b.book_Title, a.book_authors_AuthorName
FROM tbl_book b
JOIN tbl_book_authors a ON b.book_BookID = a.book_authors_BookID
WHERE a.book_authors_AuthorName = 'Author Name';
```

### Count copies in each branch

```sql
SELECT b.book_Title, bc.book_copies_No_of_Copies, lb.library_branch_BranchName
FROM tbl_book b
JOIN tbl_book_copies bc ON b.book_BookID = bc.book_copies_BookID
JOIN tbl_library_branch lb ON bc.book_copies_BranchID = lb.library_branch_BranchID;
```

---

## 📌 Conclusion

This SQL project provides a fully functional library database system with clean structure, strong relationships, and practical real-world scenarios. It can be extended into applications or dashboards if needed.

---

### **👤 Author: Vishal**

---


