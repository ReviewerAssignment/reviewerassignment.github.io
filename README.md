# Paper Assignment Data Collection

This project is a web application designed to collect data for constructing a benchmark dataset for paper-reviewer matching algorithms.

## Architecture

This project uses a **Serverless Architecture** to be compatible with GitHub Pages:

- **Frontend**: Static HTML/JS/CSS hosted on GitHub Pages.
- **Backend/Database**: [Supabase](https://supabase.com) (PostgreSQL) handles data storage directly from the frontend via the JS Client.

## Project Structure

- `index.html`: The main entry point of the application.
- `data/`: (Legacy) Local data folder, no longer used in production.

## Setup & Run Locally

1. **Clone the repository.**
2. **Open `index.html`** directly in your browser.
   - Alternatively, you can use a simple HTTP server.

## Deployment (GitHub Pages)

1. Go to your GitHub Repository settings.
2. Navigate to **Pages**.
3. Under **Source**, select `Deploy from a branch`.
4. Select `main` branch and `/root` folder.
5. Your site will be available at `https://<username>.github.io/<repo>/`.

## Data Storage

Data is stored in a Supabase table named `submissions` with the following schema:
- `email`: Text
- `profile_link`: Text
- `own_papers`: JSONB Array
- `read_papers`: JSONB Array
