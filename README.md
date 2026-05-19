# Trakr Backend

Rails API for the [Trakr](https://github.com/courtamos/final-frontend) job application tracker.

## Prerequisites

- Ruby 3.3 (`brew install ruby@3.3`)
- PostgreSQL (`brew install postgresql@14` and `brew services start postgresql@14`)

Add Ruby to your shell (once):

```sh
echo 'export PATH="/opt/homebrew/opt/ruby@3.3/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

## Setup

```sh
cd trakr-backend
bundle install
bin/rails db:create db:schema:load
```

Optional seed data:

```sh
bin/rails db:seed
```

## Run

```sh
bin/rails server
```

API runs at **http://localhost:3000** (e.g. `GET /api/logged_in`).

## Frontend

In the `trakr` repo, start the React app (`npm start` on port 8080). It proxies `/api` to this server via `src/setupProxy.js`.
