# O alemão zangado Blog — Memory

## Site
- **URL:** https://robin-wonderboy.github.io/alemao-zangado-blog/
- **Repo:** robin-wonderboy/alemao-zangado-blog
- **Local:** /Users/robin/Developer/alemao-zangado-blog/ (symlinked to projects/alemao-zangado-blog/)
- **Built with:** SiteKit (Swift static site generator by Cihat/FlineDev)
- **Deploy:** GitHub Actions → GitHub Pages (auto on push to main)

## SiteKit Gotchas
- **`language` NOT `defaultLanguage`** — docs say `defaultLanguage` but SiteKit uses `language` in SiteConfig.yaml. Using `defaultLanguage` causes `invalidYAML("The operation could not be completed. The data is missing.")` crash on Linux CI.
- **`colorScheme: "custom"` + `fontPairing: "custom"`** works fine with full token definitions
- **Content frontmatter requires `id` field** — 8-char hex, first 8 chars of UUID
- **Blog post file naming:** `YYYY-MM-DD-slug.md`
- **Tags with special chars** (like `despesas públicas`) get slugified (`despesas-publicas`)
- **Portuguese characters work fine** in content and YAML values

## Theme
- Warm orange (#C45B28 light / #E87A3A dark)
- Crimson Pro headings, Source Serif 4 body
- Warm cream background (#FAFAF5) / dark olive (#1A1A18)
- Dark mode toggle included
- Text logo "O alemão zangado" (no image logo)

## Content
- 1 blog post: "O percurso serpente" (Oct 2025)
- About page
- Home page with recent posts

## Old Repo
- `robin-wonderboy/alemao-zangado` — has messy failed build history, needs deletion (requires browser auth for `delete_repo` scope)

## TODO
- [ ] Custom domain setup
- [ ] More blog posts migrated from Blogspot
- [ ] Replace NFC.cool favicon/logo images with custom ones
- [ ] Clean up repo history (squash debug commits)
- [ ] Report `defaultLanguage` vs `language` bug to Cihat