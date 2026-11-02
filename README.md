# Vamsi — Data Analytics Portfolio

A recruiter-focused portfolio website for **Vamsi Bodigadla**, a 2026 BCA graduate pursuing entry-level data analytics and business intelligence opportunities, with a particular interest in pharma and healthcare analytics.

The site brings together project case studies, skills, education, training, a resume, and contact details. It is designed to make the work and its scope easy to review without overstating results or experience.

## What the site includes

- **Home page:** introduction, profile, principles, skills, education, certifications, resume, and contact
- **Project explorer:** search and category filters, project cards, and case-study pages
- **Project case studies:** SQL analytics, Power BI reporting, web scraping/EDA, and other portfolio projects
- **GitHub integration:** repository-based project discovery and a languages summary
- **Resume area:** view or open the PDF in a new tab
- **Admin area:** Supabase authentication, project management, publish/draft/archive states, and thumbnail uploads
- **Responsive UI:** mobile navigation, accessible interaction states, and motion/hover details

## Tech stack

- Next.js 14 and React 18
- TypeScript
- Tailwind CSS
- Supabase Auth, Postgres, Row-Level Security (RLS), and Storage
- GitHub API integration for repository discovery

## Run locally

Requirements: Node.js and npm.

1. Clone this repository and enter the project folder.
2. Install dependencies:

   ```bash
   npm install
   ```

3. Copy `.env.example` to `.env.local` and fill in the required values.
4. Start the development server:

   ```bash
   npm run dev
   ```

5. Open the local address shown by Next.js in your terminal.

To check a production build:

```bash
npm run build
```

## Supabase setup

The database migration is at `supabase/migrations/0001_init.sql`.

1. Create a Supabase project.
2. Run the migration in the Supabase SQL Editor.
3. Add the required project URL and public/anon key to `.env.local` using the variable names in `.env.example`.
4. Create the admin user in Supabase Authentication.
5. Add that user's ID to `public.admins` using the SQL documented in `PROJECT_STATUS.md`.
6. Configure the resume URL and other environment variables described by the example environment file.

The admin workflow uses the signed-in user's session and relies on Row-Level Security policies; the service-role key is not used in client-facing code.

## Current status

The codebase includes the public portfolio and an admin workflow. TypeScript checks and a production build have passed locally according to the project's development notes. **Live deployment and end-to-end testing against a production Supabase project still need to be completed.** Do not assume the site is publicly deployed just because the source code is on GitHub.

For remaining work and testing notes, see [PROJECT_STATUS.md](PROJECT_STATUS.md).

## Featured work

- [Global Retail Sales Dashboard](https://github.com/sarvendhra-vamsi/Global_Retail_Sales_Dashboard) — Power BI sales reporting
- [Music Store Management](https://github.com/sarvendhra-vamsi/Music_store_Management) — analytical SQL queries
- [Used Car Market Analysis](https://github.com/sarvendhra-vamsi/Used-Car-Market-Analysis-) — Python scraping and EDA
- [GitHub profile](https://github.com/sarvendhra-vamsi) — skills, projects, and career direction

## Project goals

This portfolio is intended to show how I approach data questions: understand the problem, check data quality, analyse carefully, and communicate findings clearly. My current focus is data analytics and BI; data engineering topics such as ingestion, staging, ETL/ELT, pipelines, and data warehousing are an active learning path.

---

**Owner:** Vamsi Bodigadla · [LinkedIn](https://www.linkedin.com/in/vamsibodigadla)
