# 🛡️ PostgreSQL Task Manager (Backend API)

This is the **Backend API** for a Task Manager application. It acts as the "Brain" of the project, handling data security, validation, and storage.

It is built with **Laravel 12** and **PostgreSQL** to demonstrate an enterprise-grade database structure (using Foreign Keys and Cascade Deletes).

---

## 🚀 Architecture
This project is decoupled (separated) into two parts:

1.  **Backend (This Repository):** * **Logic:** Laravel 12 Controllers & Routes
    * **Database:** PostgreSQL 16
    * **Role:** Provides a REST API (JSON) for the frontend to consume.

2.  **Frontend (Separate Repository):**
    * **Tech:** HTML + Vanilla JavaScript
    * **Role:** A minimal interface to test the API connection.
    * **🔗 [View the Frontend Repository Here](https://github.com/arivanismail-05/task-client-task-manager)**

---

## 🛠️ Tech Stack (Backend)
* **Framework:** Laravel 12
* **Database:** PostgreSQL (Connection via `pgsql` driver)
* **API Style:** RESTful JSON
* **Server:** Apache/Nginx (Local Development via Laragon/XAMPP)

---

## ⚙️ How to Run This Backend

1.  **Clone the Repo**
    ```bash
    git clone [https://github.com/arivanismail-05/task-manager.git](https://github.com/arivanismail-05/task-manager.git)
    cd task-manager
    ```

2.  **Setup Database**
    * Ensure PostgreSQL is running.
    * Create a database named `task_manager`.
    * Update your `.env` file with your DB credentials.

3.  **Install & Migrate**
    ```bash
    composer install
    php artisan migrate
    ```

4.  **Start Server**
    ```bash
    php artisan serve
    ```
    The API will be live at: `http://127.0.0.1:8000/api`

---

## 📝 API Endpoints
These are the routes available for the frontend to use:

| Method | Endpoint | Action |
| :--- | :--- | :--- |
| `GET` | `/api/categories` | Get all categories |
| `POST` | `/api/categories` | Create a new category |
| `DELETE` | `/api/categories/{id}` | Delete a category (and its tasks) |
| `GET` | `/api/tasks` | Get all tasks |
| `POST` | `/api/tasks` | Create a new task |
| `PUT` | `/api/tasks/{id}` | Update task (e.g., mark as done) |

---

## 💡 Note to Visitors & Challenges

This project serves as a **Backend Foundation**. I have intentionally kept the Frontend simple (Plain HTML/JS) to focus on the Backend logic.

**How to use this:**
1.  Run this backend server.
2.  Open the linked Frontend repository (`index.html`) to interact with the app.

**Challenges for You:**
I invite you to fork this repo and improve it:
* **Add Design:** The current frontend has no CSS. Feel free to add Tailwind, Bootstrap, or your own custom design to make it look professional.
* **Implement Features:** The Backend includes API routes for `Update` (PUT) and `Delete` (DELETE). Can you add buttons in the frontend to trigger these?
* **Architecture:** Try replacing the HTML frontend with a React or Vue.js application.
