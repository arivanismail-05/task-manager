# 🛡️ PostgreSQL Task Manager (Backend)

A robust, enterprise-grade REST API built with **Laravel 12** and **PostgreSQL**. This project demonstrates a clean separation of concerns, serving as the "Brain" for a separate Frontend application.

It manages **Categories** and **Tasks** using a strictly typed database schema with foreign key constraints (Cascade Deletes) and strict API validation.

---

## 🚀 Architecture
This project is the **Backend API**. It is designed to work with a decoupled Frontend.

* **Backend (This Repo):** Laravel 12 + PostgreSQL
* **Frontend:** HTML5 + Vanilla JS + Tailwind CSS
* **🔗 [View the Frontend Repository Here](https://github.com/arivanismail-05/task-client-task-manager)**

---

## 🛠️ Tech Stack
* **Framework:** Laravel 12
* **Database:** PostgreSQL 16 (The "Tank")
* **Server:** Apache/Nginx (via Laragon/XAMPP)
* **API Standard:** RESTful JSON

---

## ⚙️ Setup & Installation

**Prerequisites:** PHP 8.2+, Composer, PostgreSQL.

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/your-username/task-manager-backend.git](https://github.com/your-username/task-manager-backend.git)
    cd task-manager-backend
    ```

2.  **Install Dependencies**
    ```bash
    composer install
    ```

3.  **Configure Environment**
    * Duplicate the example file: `cp .env.example .env`
    * Open `.env` and configure your PostgreSQL settings:
        ```ini
        DB_CONNECTION=pgsql
        DB_HOST=127.0.0.1
        DB_PORT=5432
        DB_DATABASE=task_manager
        DB_USERNAME=postgres
        DB_PASSWORD=your_password
        ```

4.  **Generate Key & Migrate**
    ```bash
    php artisan key:generate
    php artisan migrate
    ```

5.  **Run the Server**
    ```bash
    php artisan serve
    ```
    The API will be available at `http://127.0.0.1:8000/api`.

---

## 📡 API Endpoints

| Method | Endpoint | Description | Payload Example |
| :--- | :--- | :--- | :--- |
| `GET` | `/api/categories` | List all categories | - |
| `POST` | `/api/categories` | Create a category | `{"name": "Work"}` |
| `GET` | `/api/tasks` | List all tasks | - |
| `POST` | `/api/tasks` | Create a task | `{"title": "Fix bug", "category_id": 1}` |

---

## 🤝 Contributing & Challenges for Visitors

This project is built as a **Solid Foundation**. It is fully functional, but purposefully lightweight to allow you to practice your skills.

**Want to contribute? Try implementing these features:**

1.  **Frontend Design:** The current frontend is minimal. Connect your own React, Vue, or polished Tailwind design to this API.
2.  **Update & Delete:** The Controller logic for `update()` and `destroy()` exists in the code, but the Frontend UI needs buttons to trigger them. Can you add them?
3.  **Authentication:** Try adding Laravel Sanctum to protect the routes so only logged-in users can manage tasks.

---

## 📝 License
This project is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
