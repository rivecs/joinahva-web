# Alabama Hemp & Vape Association (AHVA)

joinahva.com serves public advocacy and education alongside member pages and admin tools. Those areas have different access requirements, even though they live in one production site.

## Technology and decisions

- HTML, CSS, and vanilla JavaScript
- A small client-side loader for routes, shared page fragments, and page-scoped assets
- Supabase for authentication and backend services

I left out a front-end framework. The loader keeps page behavior explicit, and each page can bring its own CSS and JavaScript. The client-side checks are not the security boundary; sensitive access logic stays server-side. The site has grown through small production changes rather than a risky one-shot rewrite.

This public repository contains project notes, not the production site source.

## Links

- [AHVA](https://joinahva.com)
- [Project overview](https://github.com/rivecs/joinahva-web/blob/main/overview.md)
- [Technical decisions](https://github.com/rivecs/joinahva-web/blob/main/decisions.md)
- [Portfolio notes](https://portfolio.aerovisus.com/#ahva)
