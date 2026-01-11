# Project Overview

joinahva.com is a production website built for the non-profit Alabama Hemp & Vape Association - AHVA (Hemp & Vape Advocacy). Its primary role is to deliver public-facing advocacy content while supporting authenticated member access and administrative workflows.

This project was built under real constraints: evolving requirements, performance expectations, limited tolerance for breakage, and the need for long-term maintainability. It is not a demo project and was never intended to be one.

## Scope

The site supports three primary access levels:

- **Public**: Educational and advocacy content available to all visitors
- **Member**: Authenticated content restricted to approved users
- **Admin**: Internal tools and pages for site management

Each access level is treated as a first-class concern in both routing and asset loading.

## High-level structure

- Pages are composed from HTML partials loaded dynamically
- CSS and JavaScript are scoped per page whenever possible
- Shared functionality (navigation, auth state, redirects) is centralized
- Authentication and role checks occur before protected content loads

This structure allows new pages and features to be added without unintentionally impacting unrelated areas of the site.

## Goals

- Predictable behavior across browsers
- Minimal global side effects
- Clear separation of concerns
- Easy debugging without build tooling
- Incremental improvement over time

The emphasis is on stability and clarity rather than novelty.

## Non-goals

- Rebuilding the site as a single-page application
- Introducing heavy frameworks or build steps
- Optimizing for developer hype or trends

This project prioritizes ownership and control over abstraction.

## Live Site

https://joinahva.com

## My Site

htts://aerovisus.com

