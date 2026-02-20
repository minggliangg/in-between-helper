# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

- `bun run dev` — Start dev server with HMR
- `bun run build` — Type-check (`tsc -b`) then Vite production build
- `bun run lint` — Run ESLint
- `bun run preview` — Preview production build locally

No test runner is configured yet.

## Architecture

Single-page React 19 app bundled with Vite 8 (beta). Entry: `index.html` → `src/main.tsx` → `src/App.tsx`.

- `src/` — All application source (TypeScript/TSX)
- `public/` — Static assets served at root
- `vite.config.ts` — Vite config (currently minimal, just `@vitejs/plugin-react`)
- `tsconfig.app.json` — TS config for app source; `tsconfig.node.json` — for Vite config itself

Package manager: **bun** (lockfile is `bun.lock`).
