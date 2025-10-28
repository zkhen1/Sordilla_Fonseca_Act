📚 Library Reservation
📝 Description / Overview

The Library Reservation is a web-based application designed to help students and library staff efficiently manage book reservations and availability. It allows users to search, reserve, and track books online, reducing manual paperwork and improving the overall library experience.

This project demonstrates the use of PHP, HTML, CSS, JavaScript, and MySQL to create a functional and interactive reservation platform.

🎯 Objectives

To develop a user-friendly system for managing library book reservations.
To apply CRUD (Create, Read, Update, Delete) operations using PHP and MySQL.
To understand and practice Git and GitHub collaboration for version control.
To enhance user experience through a responsive and accessible interface.
To automate library processes and minimize manual errors.

⚙️ Features / Functionality

🧾 Book Reservation: Users can search for available books and reserve them.
👤 User Registration & Login: Secure login for students and admin accounts.
📚 Book Management: Admins can add, update, or delete book records.
🗓️ Reservation Tracking: Displays active and completed reservations.
🔍 Search Functionality: Quickly find books by title, author, or category.


💻 Installation Instructions

Follow these steps to set up and run the project locally:

Clone the Repository:
git clone https://github.com/yzkhen1/LibraryReservation.git

Navigate to Project Directory:
cd LibraryReservation

Move Files to Local Server Directory (e.g., XAMPP htdocs):
Copy the project folder into C:\xampp\htdocs\

Create the Database:
Open phpMyAdmin and create a database named library_system.
Import the provided SQL file (library_system.sql) into the database.

Run the Project:
Open your web browser and go to:
http://localhost/library-reservation-system/


🧠 Usage

Launch the project using your local server.
Login using admin credentials or register a new user account.
Search for a book and click Reserve to make a reservation.
View and manage reservations from the dashboard.
Admins can update, delete, or approve reservations.

💻Screenshots or Code Snippets

// Example: Save new reservation
if (isset($_POST['reserve'])) {
    $book_id = $_POST['book_id'];
    $user_id = $_SESSION['user_id'];
    $date_reserved = date('Y-m-d');

    $query = "INSERT INTO reservations (book_id, user_id, date_reserved, status)
              VALUES ('$book_id', '$user_id', '$date_reserved', 'Pending')";
    mysqli_query($conn, $query);
}

👩‍💻 Contributors
Kenneth M. Fonseca

⚖️ License

This project is licensed under the MIT License.
You are free to use, modify, and distribute this project for educational purposes.
