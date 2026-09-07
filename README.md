# Toan Tran's Portfolio — macOS Desktop UI

A personal portfolio site styled as a macOS desktop: a menu bar with a live clock, a dock, Finder-style project folders, an About Me window, a resume viewer, a photo gallery, a Safari-style blog reader, and a Terminal-style tech stack list.

Built with React, Vite, and Tailwind CSS.

## Features

- **Menu bar** — logo, nav links (Projects, Contact, Resume), status icons (wifi, search, user, mode), and a live clock
- **Dock** — quick-launch icons for Portfolio, Articles, Gallery, Contact, Skills, and Archive
- **Finder-style project explorer** — each project opens as a folder with a description file, a live demo link, a screenshot, and a design link
- **About Me window** — photos plus a short bio
- **Resume window** — embedded PDF viewer
- **Photos** — a gallery with sidebar categories (Library, Memories, Places, People, Favorites)
- **Safari-style blog feed** — a curated list of articles
- **Terminal-style tech stack** — skills grouped by category
- **Trash** — a hidden easter-egg folder

## Tech Stack

- [React 19](https://react.dev/)
- [Vite](https://vitejs.dev/)
- [Tailwind CSS v4](https://tailwindcss.com/) via `@tailwindcss/vite`
- [dayjs](https://day.js.org/) for the live clock
- ESLint

## Getting Started

**Prerequisites:** Node.js 18+ and npm

```bash
git clone <your-repo-url>
cd Mac_OS_Porfolio
npm install
npm run dev
```

Then open [http://localhost:5173](http://localhost:5173) in your browser.

Other available scripts:

```bash
npm run build     # production build
npm run preview   # preview the production build locally
npm run lint      # run ESLint
```

## Project Structure

```
public/
  icons/       UI icons (wifi, search, user, mode, social icons, ...)
  images/      wallpaper, logo, project screenshots, gallery photos
  files/       resume PDF
src/
  components/  React components (Navbar, ...)
  constants/   All site content — nav links, dock apps, projects, about me,
               resume, tech stack, socials, gallery
  App.jsx      Root layout
  main.jsx     App entry point
  index.css    Tailwind theme, custom utilities, and component styles
```

## Customizing Content

Every piece of text and every link on the site is data-driven from `src/constants/index.js`, so you can personalize the whole portfolio without touching component code:

- `navLinks` / `navIcons` — menu bar items
- `dockApps` — dock icons and labels
- `locations.work` — project folders shown in Finder, each with a description, live demo link, screenshot, and design link
- `locations.about` — About Me photos and bio text
- `locations.resume` — the resume PDF entry
- `techStack`, `socials`, `blogPosts`, `photosLinks`, `gallery` — the remaining sections

Drop matching images or icons into `public/images` or `public/icons` as you update these.

## Status

This project is under active development.

- [x] Menu bar
- [ ] Dock
- [ ] Finder project windows
- [ ] About Me window
- [ ] Resume window
- [ ] Photos gallery
- [ ] Safari blog window
- [ ] Terminal tech stack window
- [ ] Trash window

## License

Personal portfolio project — feel free to fork and adapt it for your own site.
