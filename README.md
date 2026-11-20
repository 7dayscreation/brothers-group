# Brothers Group LLP - Static Website

A high-performance, mobile-responsive, and SEO-optimized static website for **Brothers Group LLP**, ready for deployment to **GitHub Pages**, **Cloudflare Pages**, or any static web host.

## Clean URLs & Directory Routes (Extensionless)

All pages are structured into clean directories with `index.html`, eliminating `.html` extensions from browser URLs (matching the architecture of Wisdom):

| Route / Browser URL | Static File | Description |
| :--- | :--- | :--- |
| `https://webrothers.co.in/` | `index.html` | Homepage & brand overview |
| `https://webrothers.co.in/about/` | `about/index.html` | About Brothers Group & Designated Partners |
| `https://webrothers.co.in/projects/` | `projects/index.html` | Overview of ongoing and former projects |
| `https://webrothers.co.in/b-ethics/` | `b-ethics/index.html` | B Ethics - 2 & 3 BHK Palatial Homes |
| `https://webrothers.co.in/b-ethos/` | `b-ethos/index.html` | B Ethos - 2 & 3 BHK Upscale Living & Commercial |
| `https://webrothers.co.in/b-creation/` | `b-creation/index.html` | Seven Creation project showcase |
| `https://webrothers.co.in/b-ambition/` | `b-ambition/index.html` | Ambition residential project showcase |
| `https://webrothers.co.in/construction-update/` | `construction-update/index.html` | Monthly construction updates & photo gallery |
| `https://webrothers.co.in/journal/` | `journal/index.html` | Social media, branding, and news |
| `https://webrothers.co.in/contact/` | `contact/index.html` | Site office, contact details & interactive Google Map |
| `https://webrothers.co.in/rera-policy/` | `rera-policy/index.html` | RERA compliance & registered numbers |

## Modular PHP Architecture in `_php_backup/`

The original PHP templates have been completely refactored into clean modular components in `_php_backup/` for easy maintenance:

- **Core Config & Helpers**: `_php_backup/config.php` (defines base URL prefix, asset path helper `asset()`, and navigation route helper `url()`).
- **Global Head**: `_php_backup/includes/head.php` (canonical URLs, meta tags, secure fonts, GA4 analytics tag `G-5NC3L5C86J`).
- **Modular Menu**: `_php_backup/includes/menu.php` (standalone navigation links and mobile hamburger toggle).
- **Modular Header**: `_php_backup/includes/header.php` (header branding, menu inclusion, project overlay filter, and social icons).
- **Modular Footer**: `_php_backup/includes/footer.php` (company addresses, ongoing projects list, phone links, CREDAI news, anti-copy protection, and analytics).
- **Scripts Module**: `_php_backup/includes/scripts.php` (all jQuery plugins, owl carousel, isotope, sticky kit, and popups).
- **Modular Sliders**:
  - `_php_backup/includes/sliders/slider-home.php` (Hero slider for homepage)
  - `_php_backup/includes/sliders/slider-ethos.php` (4-slide carousel for B Ethos)
  - `_php_backup/includes/sliders/slider-ethics.php` (Background video hero slider for B Ethics)
- **RERA Compliance Modal**: `_php_backup/includes/message.php` (slide-in RERA disclaimer).

## Static Regeneration

To modify any page or modular component and re-compile the static HTML:

```bash
C:\xampp\php\php.exe _php_backup\generate_static.php
```

All 11 clean pages will instantly compile to their respective directory locations with relative portable paths.

## Hosting & SEO

- **Portable Paths**: Subfolder pages use `../assets/...` and `../images/...`, ensuring the site works locally on XAMPP, on static subfolders (`/brothers-group/`), on GitHub Pages, or on custom domains.
- **Redirections**: `_redirects` includes 301 rules redirecting legacy `.php` and `.html` URLs to extensionless directory paths.
- **Sitemap**: `sitemap.xml` lists all 11 clean canonical URLs.
- **Security & Cache**: `_headers` configures modern security headers (X-Frame-Options, X-Content-Type-Options) and long-lived asset caching.
