# joinahva.com

The official website for AHVA (Hemp & Vape Advocacy).

This is a real production site built to support public education, member access, and internal administration for an advocacy organization. It was designed and developed with long-term maintainability in mind, not as a demo or experiment.

## What this site does

- Presents public-facing advocacy and educational content
- Supports member-only pages behind authentication
- Includes an admin area for managing internal workflows
- Keeps public, member, and admin functionality clearly separated

The site needed to be fast, predictable, and easy to extend without breaking unrelated parts of the system.

## Tech Used

- HTML5
- CSS3 (global styles plus page-scoped styles)
- Vanilla JavaScript
- A custom client-side loader for:
  - Injecting HTML partials
  - Dynamically loading page-specific CSS and JS
  - Handling routing and access control
- Supabase for authentication and backend services

No frontend framework was used on purpose. The goal was clarity and control rather than abstraction.

## How it’s structured

- Pages are assembled from partials instead of full reloads
- Each page can load only the CSS and JS it actually needs
- Routing distinguishes between public, member, and admin access
- Authentication and redirects are handled centrally
- Shared UI elements like navigation are reused across the site

This approach makes the site easier to debug, easier to reason about, and less fragile as it grows.

## Design and development approach

This project reflects real production tradeoffs:

- Choosing simplicity over trendy stacks
- Optimizing for maintainability instead of speed of initial development
- Writing defensive code because content, requirements, and contributors change

It was built incrementally and refactored as needed, the way most real websites actually are.

## Live Site

https://joinahva.com

## My Site

https://aerovisus.com
