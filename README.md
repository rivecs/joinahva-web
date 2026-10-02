# joinahva.com

I built AHVA’s production site to keep public advocacy and education, member pages, and admin workflows in one system with clear boundaries between them.

## Technology

- HTML and CSS
- Vanilla JavaScript
- Supabase for authentication and backend services
- A small client-side loader for shared page fragments, routing, page-scoped CSS and JavaScript, and access checks

## Build decisions

I kept the front end framework-free because I wanted control and code that is easy to trace when something changes. Page-scoped styles and scripts keep unrelated pages from interfering with one another.

I evolved the production site in small steps instead of risking a one-shot rewrite. Sensitive logic stays server-side, and client-side access checks are defensive rather than the security boundary.

## Links

- [AHVA](https://joinahva.com)
- [Decision log](https://github.com/rivecs/joinahva-web/blob/main/decisions.md)
- [Portfolio project notes](https://portfolio.aerovisus.com/#ahva)
