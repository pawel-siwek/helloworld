# Hello World — Specification

## Purpose and scope

A minimal static page whose only visible content is exactly `Hello World`.
It uses HTML and CSS only: no JavaScript, backend, authentication, dependencies,
build process, external resources, or interactive controls.

## Requirements

- Use semantic `<main>` and a single `<h1>` for the greeting.
- Center the greeting on a light background with readable text and sufficient
  contrast.
- Adapt to narrow and desktop viewports without horizontal scrolling at 320 px
  or clipping the greeting at 200% zoom.
- Load CSS through a relative URL so the page works both from `file://` offline
  and when hosted from a static site, including beneath a URL subpath.
- Keep all required assets local; the page must not need a network connection.

## Target environments

Target the latest stable Chrome, Firefox, Safari, and Edge on desktop, plus
Chrome on Android and Safari on iOS. These targets do not imply support for
every device or historical browser, nor do they prove that a browser has been
tested.

## Acceptance criteria

- The only visible page text is exactly `Hello World`, presented as the one
  semantic heading inside the main content.
- The greeting is centered on a light background and remains legible at 320 px,
  desktop widths, and 200% zoom.
- The page and its stylesheet work offline from `index.html` and on static
  hosting, including from a subpath.
- No scripts, external requests, or application dependencies are required.
- Browser support is reported honestly: list environments actually checked;
  do not claim rendering tests that were not performed.

## Out of scope

Hosting or deployment, a domain, CI, APIs, native apps, and a license choice.
The intended public repository is `pawel-siwek/helloworld`; public visibility
alone does not grant an open-source license.
