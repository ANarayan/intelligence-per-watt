# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static website for the "Intelligence Per Watt" research project (Stanford). Hosted at **www.intelligence-per-watt.ai** via GitHub Pages (see `CNAME`).

## Architecture

The entire site is a single `index.html` file containing all HTML, CSS, and JavaScript inline — no build system, no dependencies, no framework. To preview changes, open `index.html` in a browser. Portrait photos and sponsor logos live in `img/people/` and `img/sponsors/`.

The page uses a tabbed layout with six panels (Vision, Agenda, Our Work, Related, People, Sponsors) controlled by vanilla JS that toggles `.active` classes. The layout is a CSS Grid sidebar + main content area, with responsive breakpoints at 900px and 600px.

## Key Conventions

- All styles are in a single `<style>` block; all scripts in a single `<script>` block at the end of the body
- Design uses monospace fonts (SF Mono stack), muted grayscale palette (#f0f0f0 background, #fff main content)
- Typography is small and uppercase-heavy (10-14px, `text-transform: uppercase`, wide `letter-spacing`)
- Mobile: sidebar becomes a fixed top nav with horizontally scrollable tab buttons; research table and pub grid reflow to single-column
