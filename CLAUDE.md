# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Commands

- `bun dev` - Start the Next.js development server on http://localhost:3000
- `bun run build` - Build the application for production
- `bun start` - Start the production server
- `bun run lint` - Run ESLint to check for code issues

## Project Architecture

This is a Next.js 15 application with TypeScript using the App Router pattern. The project structure follows Next.js conventions:

- **App Router**: Uses the new `app/` directory structure for routing
- **Styling**: Tailwind CSS v4 with PostCSS configuration
- **Fonts**: Geist Sans and Geist Mono from Google Fonts with CSS variables
- **TypeScript**: Strict mode enabled with path aliases (`@/*` maps to root)

### Key Files

- `app/layout.tsx` - Root layout component with font and metadata configuration
- `app/page.tsx` - Home page component
- `app/globals.css` - Global CSS with Tailwind directives
- `next.config.ts` - Next.js configuration (currently minimal)
- `tsconfig.json` - TypeScript configuration with strict mode and Next.js plugin
- `eslint.config.mjs` - ESLint configuration extending Next.js rules

### Styling System

- Uses Tailwind CSS v4 with the new PostCSS plugin architecture
- Custom CSS variables for Geist fonts: `--font-geist-sans` and `--font-geist-mono`
- Dark mode support is implemented via Tailwind's dark mode classes
- Responsive design patterns using Tailwind's responsive prefixes

### Development Notes

- The project uses Bun as the package manager (indicated by `bun.lock`)
- ESLint is configured to work with Next.js TypeScript projects
- The app follows Next.js App Router conventions for file-based routing
- Images are handled through Next.js Image component with SVG assets in `public/`