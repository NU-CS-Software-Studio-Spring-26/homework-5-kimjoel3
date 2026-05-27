# Rails 8 Todo App - Developer Guide

## Stack & Build Commands
- **Stack:** Rails 8 sample todo app, SQLite, Hotwire/Turbo, Bootstrap, RSpec
- **Setup:** `bin/setup`
- **Run dev server:** `bin/dev`
- **Run tests:** `bundle exec rspec` (or `bin/rails test`)
- **Linting:** `bundle exec rubocop`

## Conventions
- Prefer Turbo Streams over custom JavaScript for dynamic UI updates.
- Keep database migrations strictly reversible.
- Always use Rails strong parameters in controllers.
- Use `bin/rails generate` rather than hand-writing boilerplate.
- Keep the schema scoped entirely to the todo app.



## Security Rules (CRITICAL)
- Never write, log, or echo secrets, API keys, or production credentials.
- NEVER use `eval()` on user input.
- Do not use `html_safe` or `raw` on untrusted or user-provided input.
- Always use parameterized queries; never string-interpolate SQL.
- Do not disable CSRF protection, mass assignment protection, or Devise session checks.



## Project Prohibitions (Don'ts)
- No new gems without explicit approval.
- No inline JavaScript inside ERB templates.
- Never use `skip_before_action :verify_authenticity_token`.
- Do not seed real user data; use `db/seeds.rb` only.