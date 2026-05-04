## 🛡️ Authentication & Security

  Memoir-Notes utilizes **Better Auth** for a secure, enterprise-grade authentication experience:

  - **Middleware Protection**: Routes under `/dashboard` are protected; unauthenticated users are automatically redirected to `/login`.
  - **Schema**: Sessions, Users, and Accounts are managed via Drizzle in your Postgres database.
  - **Password Reset**: Integrated flow using Resend to send secure, time-limited reset links.
  - **Verification**: Email verification required to ensure valid user accounts.

---

## 🏗️ Future Roadmap

*   [ ] Full-text search across all notebooks using `nuqs`.
*   [ ] Image upload support within the Tiptap editor.
*   [ ] Bidirectional note linking (Backlinks).
*   [ ] PDF export functionality for notes.

---

# 📔 Memoir-Notes

**Memoir-Notes** is a high-performance, developer-centric note-taking application designed for the modern web. Built with **Next.js 15**, **Drizzle ORM**, and **Better Auth**, it provides a "local-first" feel with a powerful rich-text editing experience, seamless notebook organization, and robust security.

[Explore the Code](https://github.com/TheOrcDev/memoir-notes) | [Live Demo](#) 

---

## 🚀 Key Features

*   **Smart Rich-Text Editor**: Powered by **Tiptap**, supporting Markdown-style shortcuts, code blocks, and real-time auto-saving.
*   **Hierarchical Organization**: Create **Notebooks** to categorize your thoughts and **Notes** to capture specific technical insights.
*   **Secure Authentication**: Comprehensive auth flow including Google Social Login, Email/Password, and Email Verification via **Better Auth**.
*   **Modern UI/UX**: A beautiful, responsive interface built with **Tailwind CSS 4.0**, **Shadcn UI**, and **Magic UI** particles.
*   **Local-First Feel**: Optimized with **Turbopack** and **Next.js Server Actions** for near-instant interactions.
*   **Dark Mode**: Native support for light and dark themes with system preference detection.

---

## 🛠️ Technology Stack

| Category | Technology |
| :--- | :--- |
| **Framework** | [Next.js 15](https://nextjs.org/) (App Router & Turbopack) |
| **Database** | [Neon Postgres](https://neon.tech/) (Serverless) |
| **ORM** | [Drizzle ORM](https://orm.drizzle.team/) |
| **Auth** | [Better Auth](https://www.better-auth.com/) |
| **Editor** | [Tiptap](https://tiptap.dev/) |
| **Styling** | [Tailwind CSS 4.0](https://tailwindcss.com/), [Shadcn UI](https://ui.shadcn.com/) |
| **Animations** | [Motion (Framer Motion)](https://motion.dev/), [Magic UI](https://magicui.design/) |
| **Emails** | [Resend](https://resend.com/) & [React Email](https://react.email/) |
| **State/Query** | [Zod](https://zod.dev/) & [nuqs](https://nuqs.47ng.com/) (URL-state management) |

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
*   **Node.js** (v18.17 or higher)
*   **npm** / **pnpm** / **bun**
*   A **Neon Database** (PostgreSQL) connection string.
*   A **Resend API Key** for transactional emails.
*   **Google OAuth Credentials** (for social login).

---

## ⚙️ Installation & Setup

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/Vishwas-0612/Memoir-Notes.git](https://github.com/Vishwas-0612/Memoir-Notes.git)
    cd memoir-notes
    ```

2.  **Install Dependencies:**
    ```bash
    npm install
    # or
    pnpm install
    ```

3.  **Environment Variables:**
    Create a `.env.local` file in the root directory and add the following:
    ```env
    # Database
    DATABASE_URL=your_postgresql_connection_string

    # Better Auth
    BETTER_AUTH_SECRET=your_auth_secret
    NEXT_PUBLIC_BASE_URL=http://localhost:3000

    # OAuth Providers
    GOOGLE_CLIENT_ID=your_google_client_id
    GOOGLE_CLIENT_SECRET=your_google_client_secret

    # Email (Resend)
    RESEND_API_KEY=your_resend_key
    ```

4.  **Database Migration:**
    Push your schema to the database using Drizzle Kit:
    ```bash
    npx drizzle-kit push
    ```

5.  **Run Development Server:**
    ```bash
    npm run dev
    ```
    Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

---

## 📂 Project Structure
```text
├── app/                  # Next.js App Router (Pages, API, Layouts)
├── components/           # React Components (UI, Forms, Editor)
│   ├── ui/               # Reusable Shadcn UI components
│   ├── forms/            # Auth and data-entry forms
│   └── emails/           # React Email templates (Verification/Reset)
├── db/                   # Database connection and Drizzle schemas
├── hooks/                # Custom React hooks (use-mobile, etc.)
├── lib/                  # Utility functions and shared config (Auth, Utils)
├── server/               # Server Actions (CRUD for Notebooks/Notes)
└── public/               # Static assets (Logos, Icons)

```
---

**Built with ❤️by [Vishwas Srivastava](https://github.com/Vishwas-0612/Memoir-Notes)**
