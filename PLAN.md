# Hello World implementation plan

## Goal and current state

Build the static page described in [SPEC.md](SPEC.md): only `Hello World`,
centered on a light background, using HTML and CSS without dependencies.
It must work offline and on static hosting, including under a URL subpath.

The specification and static page implementation are complete. Structural
checks, an HTTP subpath check, and a Chromium smoke check passed; viewport and
200% zoom rendering checks remain unverified. Publishing these files is not a
hosting deployment.

## Team: three agents and one coordinator

| Role | Ownership | Deliverable |
| --- | --- | --- |
| Agent 1: specification and documentation | `SPEC.md`, `README.md` | Requirements, acceptance criteria, and usage instructions |
| Agent 2: implementation | `index.html`, `styles.css` | Minimal responsive page matching the specification |
| Agent 3: verification | Read-only checks | Findings and an explicit PASS, FAIL, or NOT RUN for each check |
| Coordinator | Integration and Git/GitHub operations | Consistent scope, resolved findings, and verified publication |

Agents work sequentially: documentation, implementation, then verification.
The coordinator sends defects back to the responsible agent and verifies
their resolution before declaring the application complete.

## Work items and dependencies

1. Publish the existing specification, README, and this plan to the public
   `pawel-siwek/helloworld` repository.
2. Agent 2 reads the completed specification and creates `index.html` and
   `styles.css`. Include UTF-8, an English document language, viewport metadata,
   a page title, and one `h1` inside `main`. Use a relative stylesheet URL and
   no external resources, scripts, or dependencies.
3. Agent 3 checks the implementation and documentation against the
   specification after implementation is ready.
4. The coordinator resolves findings with the responsible agents. Update the
   README status and instructions to match the delivered application.
5. Commit and push the verified implementation without overwriting remote
   history. Confirm the remote commit and files before reporting success.

The initial documentation publication does not depend on completing the
application. Application publication does depend on implementation,
verification, and integration.

## Verification

- Check the exact visible greeting, semantic structure, and readable contrast.
- Check 320 px and desktop widths and 200% zoom without clipping or horizontal
  scrolling.
- Check local offline opening and CSS loading.
- Check HTTP serving at both the root and a subpath.
- Check for unwanted network requests, scripts, and console errors.
- Report browsers and devices actually exercised; distinguish inspection
  from rendering tests. Target browsers are not a claim of completed tests.
- Use available tools without adding a test framework for a constant heading.
  Report unavailable checks and obtain a decision before claiming full
  acceptance.

## Boundaries

No backend, authentication, JavaScript, build system, Docker, native apps,
CI, hosting deployment, domain, or license selection.

A separate personal Copilot CLI agent, `adwokat-diabla`, is planned outside
this repository. It reviews explicitly supplied context and plans only when
the user invokes it, using read/search access without editing. It challenges
assumptions and unnecessary complexity with evidence, but may conclude that
there are no material issues. It neither changes the three-agent team nor
blocks this documentation publication.
