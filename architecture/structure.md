🧱 1. Server & Environment Setup

| Component            | Description                         | Example                                                                     |
| -------------------- | ----------------------------------- | --------------------------------------------------------------------------- |
| **Web Server**       | Handles HTTP requests               | Apache or Nginx                                                             |
| **Database**         | Stores WordPress content & settings | MySQL or MariaDB                                                            |
| **PHP Runtime**      | Runs the WordPress PHP code         | PHP 8.1 or higher                                                           |
| **PHP Extensions**   | Required for full functionality     | `curl`, `mbstring`, `xml`, `zip`, `gd`, `mysqli`, `json`, `intl`, `imagick` |
| **File Permissions** | For uploads, updates, etc.          | `755` directories, `644` files                                              |
| **Domain + SSL**     | For production                      | Use Let’s Encrypt or Cloudflare SSL                                         |

⚙️ 2. Core WordPress Files

| Folder         | Purpose                                          |
| -------------- | ------------------------------------------------ |
| `/wp-admin`    | Dashboard & admin interface                      |
| `/wp-includes` | Core libraries & functions                       |
| `/wp-content`  | Your editable content (themes, plugins, uploads) |


🧩 3. wp-content Structure

| Path                      | Description                      |
| ------------------------- | -------------------------------- |
| `/wp-content/themes/`     | Your **custom or chosen theme**  |
| `/wp-content/plugins/`    | Custom or installed plugins      |
| `/wp-content/uploads/`    | Media files (images, PDFs, etc.) |
| `/wp-content/mu-plugins/` | Must-use plugins (auto-loaded)   |
| `/wp-content/languages/`  | Language packs and translations  |

🎨 4. Theme Development (Frontend)

mytheme/
├── style.css
├── index.php
├── functions.php
├── header.php
├── footer.php
├── sidebar.php
├── page.php
├── single.php
├── archive.php
├── 404.php

Key Theme Files:

style.css → Theme metadata + styling.

functions.php → Enqueue scripts, define theme features.

index.php → Fallback template for all pages.

header.php / footer.php → Reusable layout parts.

page.php, single.php, archive.php → Specific templates.

screenshot.png → Preview image for dashboard.

_____________________________________________________________________

🧠 5. Plugin System (Backend Functionality)

myplugin/
├── myplugin.php
├── includes/
│   └── helper-functions.php
├── assets/
│   ├── js/
│   └── css/

Common plugin components:

    - Hooks (add_action, add_filter)

    - Custom post types

    - Shortcodes

    - Admin pages

    - AJAX handlers

    - REST API endpoints

_____________________________________________________________________

🧭 6. Configuration Files

| File                     | Description                                     |
| ------------------------ | ----------------------------------------------- |
| **`wp-config.php`**      | Connects to DB and defines settings             |
| **`.htaccess`**          | URL rewriting (for permalinks)                  |
| **`robots.txt`**         | SEO crawling rules                              |
| **`php.ini` (optional)** | Adjust PHP settings (upload size, memory, etc.) |

🧰 7. Optional Enhancements

| Category            | Example Components                                        |
| ------------------- | --------------------------------------------------------- |
| **Security**        | Wordfence, iThemes Security, custom `wp-config` hardening |
| **Caching**         | WP Super Cache, W3 Total Cache, or server-level caching   |
| **SEO**             | Yoast SEO or Rank Math                                    |
| **Backup**          | UpdraftPlus or manual database dump                       |
| **Performance**     | CDN (Cloudflare), image compression (Smush, Imagify)      |
| **Analytics**       | Google Site Kit or self-hosted tracking                   |
| **Spam Protection** | Akismet, reCAPTCHA                                        |
| **Email SMTP**      | Post SMTP (OAuth2 ready)                                  |

🔌 8. Developer Tools

| Tool                  | Purpose                                         |
| --------------------- | ----------------------------------------------- |
| **WP-CLI**            | Manage WordPress via terminal                   |
| **Composer**          | Manage PHP dependencies (for advanced builds)   |
| **Node.js**           | For theme asset bundling (SASS, Tailwind, etc.) |
| **Git**               | Version control                                 |
| **Local WP / Docker** | Local testing and development                   |


🧱 9. Database Tables (Created Automatically)

| Table                                                   | Purpose                                               |
| ------------------------------------------------------- | ----------------------------------------------------- |
| `wp_posts`                                              | All content (pages, posts, attachments, custom types) |
| `wp_postmeta`                                           | Metadata for posts                                    |
| `wp_users`                                              | User data                                             |
| `wp_usermeta`                                           | User metadata                                         |
| `wp_options`                                            | Global settings                                       |
| `wp_terms`, `wp_term_taxonomy`, `wp_term_relationships` | Categories/tags                                       |
| `wp_comments`, `wp_commentmeta`                         | Comments                                              |
| `wp_links`                                              | (Old system, rarely used)                             |
