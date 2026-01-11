# Technical Decisions

This document outlines the major technical decisions made during the development of joinahva.com and the reasoning behind them.

## No frontend framework

The site uses plain HTML, CSS, and vanilla JavaScript.

**Why:**
- Full control over behavior and performance
- No framework lock-in
- Easier debugging in production
- Lower long-term maintenance cost

Frameworks solve many problems, but they also introduce complexity that was unnecessary for this project’s requirements.

## Custom loader system

A custom client-side loader handles:
- Route-based page loading
- Partial HTML injection
- Page-scoped CSS and JS
- Access control for public, member, and admin pages

**Why:**
- Prevents global CSS/JS bleed
- Reduces unnecessary asset loading
- Keeps page behavior explicit
- Makes failures easier to isolate

This approach trades convenience for predictability.

## Page-scoped assets

Each page can define its own CSS and JavaScript files.

**Why:**
- Avoids “mystery styles” affecting unrelated pages
- Encourages modular thinking
- Reduces regression risk when making changes

Global styles are kept intentionally small and conservative.

## Incremental refactoring over rewrites

The site was improved and reorganized over time rather than rebuilt all at once.

**Why:**
- Production sites rarely allow clean rewrites
- Incremental changes reduce risk
- Easier to validate behavior after each change

This reflects how real-world systems evolve.

## Supabase for auth and backend services

Supabase is used for authentication and related backend needs.

**Why:**
- Reduces custom backend maintenance
- Provides reliable auth flows
- Integrates cleanly with frontend-only architecture

Sensitive logic remains server-side, while the frontend enforces access defensively.

## Design priorities

- Clarity over cleverness
- Consistency over experimentation
- UX decisions that support content, not decoration

Visual polish and usability were treated as core requirements, not afterthoughts.

## Tradeoffs accepted

- Slightly more manual wiring in exchange for transparency
- Fewer abstractions in exchange for control
- More discipline required from future contributors

These tradeoffs were deliberate and align with the long-term goals of the project.

## Live Site

https://joinahva.com

## My Site

https://aerovisus.com

