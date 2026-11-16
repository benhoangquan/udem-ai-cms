# UdeM AI CMS

Sanity Studio for the UdeM AI club website (v2): schemas for members, activities, posts, resources, opportunities and general club info. The Studio host is `udemai` (`sanity.cli.ts`).

This repo is no longer in use. The club site now reads Markdown content ([udem_ai_website_v2](https://github.com/benhoangquan/udem_ai_website_v2), then [udem_ai_website_v3](https://github.com/benhoangquan/udem_ai_website_v3)), so this Studio no longer feeds a frontend.

## Architecture

| Path | Contents |
|---|---|
| `schemaTypes/documents/` | `activity`, `generalInfo`, `member`, `opportunity`, `post`, `resource` |
| `schemaTypes/objects/` | `blockContent`, `code`, `contactInfo`, `location`, `resourceCategory`, `socialLinks` |
| `scripts/` | Per-type seed scripts that write fake records with `@faker-js/faker`, a `createData.ts` runner, and a schema validator |
| `.github/workflows/sanity_CI.yaml` | Lint, type check and `npm test` on pushes and pull requests |

## Quickstart

```bash
npm ci
npm run dev        # local Studio
npm test           # lint + type check
```
