# 🛣️ Laravel Learning Roadmap

## 🟢 Phase 1: PHP & Web Fundamentals
> Before learning Laravel, you need a solid foundation in PHP and general web development.

- ✅ HTML, CSS, and basic JavaScript  
- ✅ Basic PHP (variables, functions, loops, OOP)  
- ✅ Understanding of HTTP (GET, POST, session, cookie)  
- ✅ MySQL (SELECT, INSERT, UPDATE, JOIN, Index, etc.)  
- ✅ Composer – PHP dependency manager  

---

## 🟡 Phase 2: Laravel Basics
> Start learning Laravel once you’re comfortable with PHP.

- ✅ Installing Laravel via Composer  
- ✅ Laravel folder structure  
- ✅ Routing  
- ✅ Controllers – handle business logic  
- ✅ Views (Blade templates) – display data  
- ✅ Request & Response  
- ✅ Migrations & Seeders – manage the database  
- ✅ Models & Eloquent ORM – interact with the DB easily  
- ✅ Validation – check user input  
- ✅ Session & Flash Messages  

---

## 🟠 Phase 3: Intermediate Laravel
> Learn deeper concepts to build more robust and maintainable applications.

- ✅ Middleware – process logic before/after requests  
- ✅ Authentication (login, register, password reset)  
- ✅ Authorization (Gates & Policies)  
- ✅ Building APIs with Laravel (API routes, Postman testing)  
- ✅ Laravel Sanctum / Passport for API authentication  
- ✅ Events & Listeners  
- ✅ Queues & Jobs – asynchronous processing  
- ✅ File Storage – image/document uploads  
- ✅ Image upload, crop, resize with Intervention  
- ✅ Localization – multi-language support  

---

## 🔵 Phase 4: Advanced Laravel
> For large-scale or production-ready applications.

- ✅ Service Container & Service Providers  
- ✅ Repository Pattern – clean, testable code  
- ✅ Unit Testing with PHPUnit / Feature Testing  
- ✅ Laravel Livewire / Inertia.js – build SPAs easily  
- ✅ Laravel Broadcasting (real-time with Pusher)  
- ✅ Laravel Horizon – queue management  
- ✅ Laravel Telescope – request debugging and tracking  
- ✅ Laravel Octane – performance boost  

---

## 🟣 Essential Tools & Environment

- ✅ Git & GitHub/GitLab  
- ✅ Laravel Valet / Homestead / Sail / XAMPP  
- ✅ VS Code + Laravel Extensions (Laravel Snippets, Blade Formatter, etc.)  
- ✅ Postman for API testing  

---



# ✅ Laravel Best Practices

## 1. Project Structure & Organization

- Use **PSR-4 autoloading** and proper namespaces.
- Group related logic using **Service, Repository, and Interface layers**.
- Keep **controllers thin** — move business logic to Services.
- Avoid putting too much logic in routes or controllers.
- Use **Form Requests** for validation instead of inline rules in controllers.

---

## 2. Eloquent & Database

- Use **Eloquent relationships** properly (`hasOne`, `hasMany`, etc.).
- Use **accessors & mutators** for formatting model attributes.
- Avoid **N+1 queries** — always eager load (`->with()`) when needed.
- Use **SoftDeletes** for important data that should be recoverable.
- Keep your migrations clean and use meaningful column names.

---

## 3. Routing & Controllers

- Use **Route model binding** to inject models automatically.
- Group routes with `prefix`, `middleware`, and `namespace` where needed.
- Follow **RESTful conventions** for route and controller naming.
- Limit controller methods to **single responsibility**.

---

## 4. Security

- Always use `bcrypt` or `Hash::make()` for password encryption.
- Protect routes with **middleware** (`auth`, `throttle`, etc.).
- Use **CSRF tokens** (`@csrf`) in all forms.
- Use **authorization policies** for permission control (`Gate`, `Policy`).
- Validate all input using **Form Request Validation**.

---

## 5. Blade Templates & Frontend

- Use `@include`, `@component`, and layout templates to avoid duplication.
- Escape all output with `{{ $var }}` to prevent XSS.
- Use `@foreach`, `@isset`, `@empty` wisely for cleaner loops and conditionals.
- Keep business logic **out of views**.

---

## 6. Performance

- Use **caching** (`config`, `route`, `view`, `query`).
- Use **queue jobs** for tasks like sending emails, processing images, etc.
- Avoid unnecessary DB calls; use caching strategies like `remember()`.
- Minimize eager loading of unused relationships.

---

## 7. Testing & Debugging

- Write **feature tests** and **unit tests** using PHPUnit.
- Use **Laravel factories & seeders** for test data.
- Use **Laravel Telescope** to monitor requests, DB, queue, etc.
- Use **Laravel Debugbar** for local development (don’t deploy it to production!).

---

## 8. Deployment & Maintenance

- Set correct permissions on `storage/` and `bootstrap/cache/`.
- Use **.env** for config separation (don’t commit this file).
- Always run:
  - `php artisan config:cache`
  - `php artisan route:cache`
  - `php artisan view:cache`
- Use **version control** (Git) and CI/CD when possible.
- Log properly using `Log::info()`, `Log::error()`, etc.

---

## 9. Naming Conventions

- **Models**: singular (`User`, `Product`)
- **Controllers**: plural (`UsersController`, `ProductsController`)
- **Table names**: plural (`users`, `products`)
- **Route names**: kebab-case (`/user-profile`)
- **Variables**: camelCase (`$userName`, `$productList`)

---

## 10. Useful Tools

- 🔧 Laravel IDE Helper  
- 🔧 Laravel Pint (code formatting)  
- 🔧 Laravel Debugbar  
- 🔧 Laravel Telescope  
- 🔧 Laravel Horizon (queue monitoring)
  
## Pratices more in [alexeymezenin/laravel-best-practices](http://github.com/alexeymezenin/laravel-best-practices)
