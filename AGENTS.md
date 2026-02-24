# PropWise CRM documentation

## About this project

- Internal technical documentation for the PropWise CRM platform (backend + frontend)
- Built on [Mintlify](https://mintlify.com) with MDX pages and YAML frontmatter
- Configuration lives in `docs.json`
- Run `mint dev` to preview locally
- Run `mint broken-links` to check links

## Site structure

| Tab | Audience | Content |
|-----|----------|---------|
| **Getting started** | All developers | Overview and onboarding |
| **Backend** | Backend developers | NestJS architecture, CRM module, access control, real estate, performance |
| **Frontend** | Frontend developers | React patterns, TanStack Query, RBAC, component extraction |

## Terminology

- Use "organization" not "company" when referring to tenants (Company is a CRM entity)
- Use "stakeholder" not "assignee" for entity assignment relationships
- Use "pool lead" not "unassigned lead" for leads in team/global pools
- Use "access level" not "permission level" for stakeholder READ/WRITE/FULL
- Use "resource permissions" not "response permissions" when referring to `ResourcePermissionsDto`

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings: "Core concepts", not "Core Concepts"
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references
- No emoji in documentation content

## Mintlify component requirements

Every `.mdx` page MUST use Mintlify components where applicable. Do NOT fall back to plain markdown when a component exists. See `.cursor/rules/component-enforcement.mdc` for the full substitution table and pre-completion checklist.

Key rules:
- Callouts (`<Note>`, `<Warning>`, `<Tip>`, `<Info>`) instead of blockquote workarounds
- `<Steps>` for sequential procedures
- `<Tabs>` for alternative content or entity comparisons
- `<AccordionGroup>` for long checklists or optional reference sections
- `<CardGroup>` for "Related documentation" links
- No manual table of contents (Mintlify auto-generates it)

## Content boundaries

- This documents the PropWise CRM system architecture and patterns for internal developers
- Do NOT document deployment infrastructure, CI/CD pipelines, or cloud provider setup
- Do NOT include real API keys, database credentials, or production URLs
- Each page mirrors a `Docs/*.md` specification file from the backend or frontend repo
