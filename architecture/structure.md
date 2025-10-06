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
