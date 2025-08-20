# Laravel-Login

A Laravel-based web application featuring a user authentication system. Users can register, log in, log out, and manage sessions using Laravel’s built-in auth scaffolding.

##  Features

-  User registration and login  
-  Password hashing and “remember me” functionality  
-  Secure logout  
-  Session management and CSRF protection  
-  Customizable authentication views and routes

##  Tech Stack

- **Framework**: Laravel (e.g., 10.x or latest) – a modern PHP MVC framework :contentReference[oaicite:0]{index=0}  
- **Language**: PHP 8+ (recommended)  
- **Auth Scaffolding**: Laravel Breeze, Jetstream, or Fortify (choose whichever you’ve used) :contentReference[oaicite:1]{index=1}

##  Prerequisites

- PHP 8.1 or higher  
- Composer  
- MySQL / PostgreSQL / SQLite  
- Node.js & npm (if using frontend scaffolding like Tailwind)

##  Installation & Setup

1. **Clone the repository**  
   ```bash
   git clone https://github.com/DinukaEk/Laravel-Login.git
   cd Laravel-Login

2. **Install dependencies**
   ```bash
   composer install
   npm install && npm run dev  # if frontend scaffolding is present

3. **Configure environment**
   ```bash
   cp .env.example .env
   php artisan key:generate
  Update .env with your database credentials (DB_CONNECTION, DB_HOST, etc.).
   
4. **Run migrations**
   ```bash
   php artisan migrate
   
5. **(Optional) Install authentication scaffolding**
   For Laravel 10 with Breeze:
   ```bash
   composer require laravel/breeze --dev
   php artisan breeze:install
   npm install && npm run dev
   php artisan migrate
   
6. **Run the application**
    ```bash
    php artisan serve
  Visit http://localhost:8000 to access the app.


## Project Structure
```bash
Laravel-Login/
├── app/                # Core Laravel app code (Controllers, Models, etc.)
├── config/             # Configuration files
├── database/
│   └── migrations/     # Migration scripts (e.g., create users table)
├── resources/
│   ├── views/          # Blade templates (e.g., login, register, dashboard)
│   └── css/js/         # Frontend assets (if using Breeze/Jetstream)
├── routes/
│   └── web.php         # Web routes configuration
├── .env.example        # Environment variables template
└── README.md           # This documentation
```


## Usage

1. Register a new user via /register (if scaffolding provides it).
2. Log in via /login.
3. Access protected routes or user dashboard (e.g., /home) after authentication.
4. Log out securely and invalidate the session.


## Customization Ideas

• Add email verification using Laravel’s built-in features
• Integrate social login (e.g., GitHub, Google) with Laravel Socialite
• Implement role-based access control (using policies or packages like Spatie Permissions)
• Enhance UI with Tailwind, Bootstrap, or your preferred CSS framework


## Contributing

Contributions are welcome! Here's how:
1. Fork the repository
2. Create a feature branch (git checkout -b feature/your-feature)
3. Make your changes and commit them (git commit -m "Add feature")
4. Push to your branch (git push origin feature/your-feature)
5. Open a Pull Request for review


## License

Distributed under the MIT License. See LICENSE file for details (if present).
