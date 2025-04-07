# 🛣️ Laravel Learning Roadmap (With Packages & Docs)

---

## 🟢 Phase 1: PHP & Web Fundamentals

> Before Laravel, master core PHP and web basics.

- ✅ [HTML, CSS, JavaScript](https://developer.mozilla.org/en-US/)
- ✅ [PHP Basics](https://www.php.net/manual/en/index.php)
- ✅ [HTTP Methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)
- ✅ [MySQL](https://www.mysql.com/)
- ✅ [Composer](https://getcomposer.org/)

---

## 🟡 Phase 2: Laravel Basics

> Start building with Laravel.

- ✅ [Laravel Installation](https://laravel.com/docs/installation)
- ✅ [Folder Structure](https://laravel.com/docs/structure)
- ✅ [Routing](https://laravel.com/docs/routing)
- ✅ [Controllers](https://laravel.com/docs/controllers)
- ✅ [Blade Templates](https://laravel.com/docs/blade)
- ✅ [Requests & Responses](https://laravel.com/docs/requests)
- ✅ [Migrations](https://laravel.com/docs/migrations)
- ✅ [Eloquent ORM](https://laravel.com/docs/eloquent)
- ✅ [Validation](https://laravel.com/docs/validation)
- ✅ [Sessions](https://laravel.com/docs/session)

📦 Useful packages:
- [`barryvdh/laravel-debugbar`](https://github.com/barryvdh/laravel-debugbar)
- [`spatie/laravel-permission`](https://github.com/spatie/laravel-permission)

---

## 🟠 Phase 3: Intermediate Laravel

> Level up with core Laravel features.

- ✅ [Middleware](https://laravel.com/docs/middleware)
- ✅ [Authentication](https://laravel.com/docs/authentication)
- ✅ [Authorization (Policies & Gates)](https://laravel.com/docs/authorization)
- ✅ [API Resources](https://laravel.com/docs/eloquent-resources)
- ✅ [Sanctum](https://laravel.com/docs/sanctum) / [Passport](https://laravel.com/docs/passport)
- ✅ [Events & Listeners](https://laravel.com/docs/events)
- ✅ [Queues & Jobs](https://laravel.com/docs/queues)
- ✅ [File Storage](https://laravel.com/docs/filesystem)
- ✅ [Localization](https://laravel.com/docs/localization)

📦 Useful packages:
- [`spatie/laravel-translatable`](https://github.com/spatie/laravel-translatable)
- [`intervention/image`](https://github.com/Intervention/image)
- [`fruitcake/laravel-cors`](https://github.com/fruitcake/laravel-cors)

---

## 🔵 Phase 4: Advanced Laravel

> Build production-level apps.

- ✅ [Service Container](https://laravel.com/docs/container)
- ✅ [Service Providers](https://laravel.com/docs/providers)
- ✅ [Repository Pattern (custom structure)](https://dev.to/sujaykundu777/repository-design-pattern-in-laravel-4p6b)
- ✅ [Testing](https://laravel.com/docs/testing)
- ✅ [Livewire](https://laravel-livewire.com/docs)
- ✅ [Inertia.js](https://inertiajs.com/)
- ✅ [Broadcasting](https://laravel.com/docs/broadcasting)
- ✅ [Laravel Horizon](https://laravel.com/docs/horizon)
- ✅ [Laravel Telescope](https://laravel.com/docs/telescope)
- ✅ [Laravel Octane](https://laravel.com/docs/octane)

📦 Useful packages:
- [`laravel/horizon`](https://github.com/laravel/horizon)
- [`laravel/telescope`](https://github.com/laravel/telescope)
- [`livewire/livewire`](https://github.com/livewire/livewire)
- [`inertiajs/inertia-laravel`](https://github.com/inertiajs/inertia-laravel)

---

## 🟣 Tools & Environment

- ✅ [Git](https://git-scm.com/)
- ✅ [Laravel Sail](https://laravel.com/docs/sail)
- ✅ [Laravel Valet](https://laravel.com/docs/valet)
- ✅ [Laravel Homestead](https://laravel.com/docs/homestead)
- ✅ [Postman](https://www.postman.com/)

📦 Dev Helper Packages:
- [`barryvdh/laravel-ide-helper`](https://github.com/barryvdh/laravel-ide-helper)
- [`nunomaduro/larastan`](https://github.com/nunomaduro/larastan)
- [`laravel/pint`](https://github.com/laravel/pint)

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
