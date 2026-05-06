# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This repository hosts public-facing documentation for **Chunches** — a Flutter mobile app that lets families share shopping lists, recipes, and calendar events. The primary artifact is the privacy policy, maintained in two forms:

- `policy.md` — source of truth, written in Markdown
- `policy.html` — styled HTML version served to users (e.g., linked from the App Store / Play Store listing)

## Workflow

When updating the privacy policy, edit `policy.md` first, then reflect those changes in `policy.html`. The HTML file is a self-contained page (no build step, no bundler) with all styles inlined in a `<style>` block.

## App context

- **Backend:** Supabase (database, auth, storage, Row Level Security)
- **Push notifications:** Firebase
- **Auth methods:** email/password, Google Sign-In, Apple Sign-In
- **Data model:** users belong to family groups; family content (lists, recipes, events) is shared across members
- **Contact:** fernando.herrera.apps@gmail.com
