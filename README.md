# Expense Tracker

A simple expense tracking app built with Next.js (App Router), TypeScript, and Tailwind CSS. Track incomes and expenses, categorize transactions, and view basic reports.

## Features

- Add / edit / delete transactions (amount, date, category, notes)
- Categorization and monthly summaries
- Responsive UI with Tailwind CSS
- Persist data locally with Prisma + SQLite (configurable for other databases)
- Simple charts for overview (e.g., Chart.js)

## Tech stack

- Next.js (App Router)
- TypeScript
- Tailwind CSS
- Prisma ORM + SQLite (default)
- Optional: Chart.js for visualizations

## Getting started

1. Clone the repo and install dependencies:

```bash
git clone <repo-url>
cd expense-tracker
npm install
# or yarn / pnpm install
```

2. Setup environment

Create a .env file in the project root. Example:

```env
DATABASE_URL="file:./dev.db"
NEXT_PUBLIC_BASE_URL="http://localhost:3000"
```

3. Initialize the database (Prisma + SQLite example)

```bash
npx prisma migrate dev --name init
# or, if you prefer no migrations:
# npx prisma db push
```

4. Run the development server

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open http://localhost:3000

## Available scripts

- dev — run Next.js in development
- build — build for production
- start — start production server
- lint — run ESLint
- format — run Prettier (if configured)
- prisma:migrate — apply Prisma migrations
- prisma:studio — open Prisma Studio

(These scripts are defined in package.json — adjust names/commands to match your setup.)

## Project structure (typical)

- app/ — Next.js App Router pages and layouts
- components/ — UI components
- prisma/ — schema.prisma and migrations
- lib/ — utilities (db clients, helpers)
- styles/ — global styles / Tailwind config

## Deployment

Build and deploy like any Next.js app. Vercel is recommended for quick deployments. Ensure environment variables are set in the deployment platform (DATABASE_URL, NEXT_PUBLIC_BASE_URL).

## Contributing

Contributions, issues, and feature requests are welcome. Open a PR with clear changes and tests where applicable.

## License

Specify your license (e.g., MIT) in LICENSE file.

If your project uses a different database or charting library, update the instructions and env variables accordingly.
