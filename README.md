# LedenadministratieApp

LedenadministratieApp is a modern web application for managing families, members, and contributions for associations or clubs. Built with PHP and the MVC pattern, it offers a secure, responsive, and user-friendly admin dashboard.

---

## Features

- **MVC Architecture:** Clear separation of models, views, and controllers.
- **Family Management:** Add, edit, and delete families.
- **Member Management:** Add, edit, and delete members within families.
- **Contribution Management:**
  - View, add, and delete contributions per family and year.
  - Manage discounts per family directly on the contributions page.
- **Admin Dashboard:** Secure area for administrators with full CRUD capabilities.
- **Security:**
  - CSRF protection on all forms.
  - Session checks for admin actions.
  - Passwords securely stored using password_hash.
- **Responsive Design:** Works seamlessly on desktop and mobile devices.
- **Modern Styling:** Clean, accessible, and intuitive interface.

---

## Installation

1. **Clone or download** the project to your web server (e.g., XAMPP).
2. **Database:**
   - Import the provided SQL script (if available) into your MySQL database.
   - Update the database settings in `/config/Database.php` if needed.
3. **Start your server** (e.g., via XAMPP) and navigate to `/public/assets/index.php` in your browser.

---

## Usage

- **Family Login:** Enter the unique ID, address, and family name.
- **Admin Login:** Use the admin login page. Change the admin password via the database if needed (see below).
- **Manage Families:** Add, edit, or delete families.
- **Manage Members:** Add, edit, or delete members within a family.
- **Manage Contributions:**
  - View, add, or delete contributions per family and year.
  - Adjust the discount for each family on the contributions page.

---

## Changing the Admin Password

1. Generate a new hash in PHP:
   ```php
   echo password_hash('your_new_password', PASSWORD_DEFAULT);
   ```
2. Paste the hash into the `password` field for the admin in your database.

---

## Common Issues & Solutions

- **Login not working:** Check for case sensitivity and spaces in the database. The comparison is case-insensitive.
- **Delete not working:** Ensure the CSRF token is present in the form and the correct controller handles the action.
- **Table header not fully colored:** Make sure the number of `<th>` in the header matches the number of `<td>` in the rows.

---

## Credits

- Developed by [your name/team].
- Styling inspired by modern admin templates.

---

## License

This project is open source and free to use for non-commercial purposes.
