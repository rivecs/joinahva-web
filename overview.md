# Project overview

joinahva.com is the production website for the Alabama Hemp & Vape Association. It serves three groups: visitors looking for public advocacy and educational material, members with authenticated pages, and admins who manage the site.

## Site structure

- Pages are assembled from HTML partials.
- A small loader handles routes and shared navigation and auth behavior.
- Page CSS and JavaScript are scoped so unrelated pages do not pick up each other’s changes.
- Supabase backs authentication and related backend services.

Access checks in the browser help the interface show the right pages, but they are not the security boundary. Sensitive decisions stay server-side.

## Why the site is structured this way

This is a live site with changing requirements. I chose a small, framework-free front end and incremental changes so I can trace what a page does and validate each change without turning the whole site into a rewrite.

## Links

- [AHVA](https://joinahva.com)
- [Portfolio notes](https://portfolio.aerovisus.com/#ahva)
