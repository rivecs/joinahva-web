# Technical decisions

These are the choices that shape the joinahva.com front end and how it handles a live site with public, member, and admin areas.

## Plain HTML, CSS, and JavaScript

The pages use native browser technologies rather than a front-end framework. The requirements did not call for a client-side application framework, and the smaller setup makes page behavior easier to trace in production.

## A small loader, scoped page assets

A client-side loader routes to page partials and loads each page’s CSS and JavaScript. Shared navigation and auth behavior stay centralized; page-specific code stays close to the page that uses it. This adds some manual wiring, but it limits global side effects and makes failures easier to isolate.

## Access checks and the security boundary

The interface distinguishes public, member, and admin areas. Browser checks help route people and avoid showing the wrong screen; they are not treated as the security boundary. Authentication and sensitive access logic stay in the backend, with Supabase providing authentication and related services.

## Change the production site in small steps

I have kept improving the production site incrementally instead of replacing it in one pass. That makes each change easier to inspect and lowers the risk of breaking unrelated pages.

## Links

- [AHVA](https://joinahva.com)
- [Project overview](https://github.com/rivecs/joinahva-web/blob/main/overview.md)
- [Portfolio notes](https://portfolio.aerovisus.com/#ahva)
