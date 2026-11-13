# Pongpitchit Sittipakdee — Portfolio

Personal portfolio of Pongpitchit Sittipakdee, Full-Stack Developer (Rangsit University, DIT).

Live: [pongpitchit.in.th](https://pongpitchit.in.th)

A minimal dark/light portfolio built with **Next.js 14 · TypeScript · Tailwind CSS**.

## Stack
- **Framework**: Next.js 14 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS + CSS custom properties (theme vars)
- **Fonts**: Bebas Neue (display) · Syne (sans) · DM Mono (mono)
- **Data**: `lib/portfolio-data.ts` — edit this file to update all content

## Getting Started

```bash
# 1. Install dependencies
npm install

# 2. Run development server
npm run dev

# 3. Open http://localhost:3000
```

## Project Structure

```
app/
  layout.tsx          — Root layout, metadata, ThemeProvider
  page.tsx            — Main page orchestrator (section switching)
  globals.css         — Theme variables + animations
components/
  Navbar.tsx          — Top nav with theme toggle
  Hero.tsx            — Landing / boot screen
  ProfileSection.tsx  — About, services, tech stack, education
  ProjectSection.tsx  — Project grid with category filter
  ProjectModal.tsx    — Project detail modal
  ResumeModal.tsx     — Resume preview / download (public/resume.pdf)
  ContactSection.tsx  — Socials + thank you screen
  Marquee.tsx         — Scrolling skills ticker
hooks/
  useTheme.tsx        — Dark/Light theme context
lib/
  portfolio-data.ts   — ALL content lives here (edit freely)
types/
  index.ts            — Type re-exports
public/               — Project screenshots, logos, resume.pdf
```

## Theme System

Toggle between **Dark** and **Light** themes via the top-right button.
Theme is persisted in `localStorage`; colors are CSS custom properties in `app/globals.css`.

## Adding a Project

1. Put a screenshot in `public/` (e.g. `public/my-project.png`)
2. Add an entry at the **end** of `portfolioData.projects` in `lib/portfolio-data.ts`
   (use `'#'` for `liveUrl` / `githubUrl` to hide the button)
3. The last entry is always shown first, as the large featured card

## Build for Production

```bash
npm run build
npm run start
```
