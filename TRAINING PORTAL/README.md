## Flowchart Link : https://drive.google.com/file/d/1AIb2D9KwLce6mTpqZSL7dHU6oIKnLRGw/view?usp=sharing

# Training Portal ER Diagram & Database Schema


This project contains the **Entity–Relationship (ER) diagram** and **database schema** for a **Training Portal System**.
It is designed to manage **users, trainers, courses, assessments, payments, feedback, and certifications**, with added advanced features like **badges, notifications, attendance tracking, and course categories**.

---

## Entities

* **User** – Learners, trainers, and admins of the system.
* **Department** – Organizational units where users belong.
* **Course** – Training courses offered in the portal.
* **Trainer** – Trainers conducting courses.
* **Course\_Category** – Categories for organizing courses.
* **Training\_Materials** – Learning resources with version control.
* **Payment** – Course payments and transactions.
* **Assessment** – Tests taken after courses.
* **Preassessment** – Tests taken before courses.
* **Feedback** – User feedback on courses/trainers.
* **Certificate** – Certificates awarded after course completion.
* **Badge** – Achievement system for users.
* **Notification** – System messages sent to users.
* **Attendance** – Tracks user participation in courses.

---

## Relationships

* **User ↔ Department**: A user belongs to one department (**M:1**)
* **User ↔ Course**: Users register for multiple courses (**M\:N**)
* **Course ↔ Trainer**: Each course is conducted by one trainer (**M:1**)
* **Course ↔ Category**: Each course belongs to a category (**M:1**)
* **Course ↔ Training\_Materials**: A course contains many materials (**1\:M**)
* **User ↔ Payment**: A user makes payments for courses (**1\:M**)
* **User ↔ Assessment**: A user takes multiple assessments (**1\:M**)
* **User ↔ Preassessment**: A user attempts pre-course tests (**1\:M**)
* **User ↔ Feedback**: A user gives feedback on courses/trainers (**1\:M**)
* **User ↔ Certificate**: A user earns certificates after completion (**1\:M**)
* **User ↔ Badge**: A user can earn multiple badges (**M\:N**)
* **User ↔ Notification**: A user receives multiple notifications (**1\:M**)
* **User ↔ Attendance**: Attendance is tracked per course (**1\:M**)

---

## Weak Entities

* **Attendance** → Depends on User + Course
* **User\_Badge** → Depends on User + Badge
* **Certificate** → Optional weak entity (depends on User + Course, if not independent)

---
