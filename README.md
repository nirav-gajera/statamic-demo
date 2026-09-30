# Test Company - Enterprise IT Industry Business Portfolio (Statamic Demo)

![Statamic](https://img.shields.io/badge/Statamic-v5-FF4C00)
![TailwindCSS](https://img.shields.io/badge/Tailwind%20CSS-v4-38B2AC)
![PHP](https://img.shields.io/badge/PHP-8.2%2B-777BB4)
![MIT](https://img.shields.io/badge/license-MIT-blue.svg)
![Nirav Gajera](https://img.shields.io/badge/Developer-Nirav%20Gajera-lightgrey)

A comprehensive, production-ready corporate business portfolio web application built on **Statamic v5 (Flat-File Engine)** and styled with **Tailwind CSS v4**. 

This demo showcases how an enterprise IT company (**Test Company**) can manage 100% of its website layout, raw HTML/Tailwind components, SEO metadata, global settings, and collection data dynamically via the Statamic Control Panel (`/cp`) without requiring developer code edits.

---

## 🌟 Key Highlights & Architecture

- **Zero-DB Flat-File Speed**: Content is stored in human-readable Markdown and YAML files in the `content/` directory—eliminating SQL query bottlenecks, database migrations, and database connection overhead.
- **100% CP-Manageable UI (`code_field`)**: Raw tailored HTML and Tailwind CSS utility classes are stored inside the `code_field` block (configured in `htmlmixed` mode), enabling full UI and content modification directly from the Control Panel (`/cp`).
- **Dynamic Collections & Routing**:
  - **Pages Collection**: Handles static routes (`/`, `/test-page`, `/redirect-me`).
  - **Projects Collection**: Dynamic IT case study entries routed individually at `/projects/{slug}`.
  - **Services Collection**: Enterprise IT service capabilities rendered dynamically.
- **Dynamic Navigation System**: Global header and footer menus are fully managed via Statamic's Navigation UI in `/cp`.
- **Global Settings & Branding**: Company details, footer copy, ISO certifications, and client counts are managed via Statamic Globals in `/cp`.
- **Integrated SEO & Social Meta**: Built-in SEO & Social Meta fields (`seo_title`, `meta_description`, `og_image`, `canonical_url`) with Twitter Cards and Open Graph protocol support.

---

## 📂 Project Structure & Route Overview

### 1. Web Routes & Page Structure

| URL Route | Template | Description |
| :--- | :--- | :--- |
| `/` | `home.antlers.html` | Corporate Business Portfolio homepage featuring hero section, strategic overview, services, dynamic projects grid, and contact CTA. |
| `/test-page` | `test-page.antlers.html` | **Solutions Overview & Architecture**: Enterprise IT capabilities and markdown documentation view. |
| `/projects/{slug}` | `project.antlers.html` | **Dedicated Case Study Pages**: Individual case studies (`/projects/ecommerce-redesign`, `/projects/fintech-mobile-app`, `/projects/ai-branding-campaign`) rendering unique UI blocks from `code_field`. |
| `/redirect-me` | `default.antlers.html` | **Route Traffic Jumper**: Demonstrates Statamic 302 HTTP redirection handling back to `/test-page`. |

---

## ⚙️ Control Panel Administration (`/cp`)

Access the Statamic Control Panel admin interface at **`http://statamic-demo.test/cp`** (or `http://localhost/cp`).

### 1. Managing UI Layout & Page Copy (`code_field`)
- Navigate to **Collections** -> **Pages** -> Click **Home**.
- The **Code Field** block contains the entire homepage HTML and Tailwind markup. Edit Tailwind utility classes, headings, or section structures visually in the CP and click **Save**.

### 2. Managing Dedicated Case Studies
- Navigate to **Collections** -> **Projects**.
- Select any case study (*E-commerce Platform Architecture*, *Fintech Mobile Banking Engine*, *AI Platform Cloud Infrastructure*), or click **Create Entry**.
- Fill in fields for **Title**, **Client Name**, **Year**, **Category**, **Featured Image**, and the project's unique **Case Study UI Code Block (`code_field`)**.

### 3. Managing Global Company Info & Footer Copy
- Navigate to **Globals** -> **Company Details**.
  - **Main Tab**: Edit Company Name (`Test Company`), Industry (`IT Industry Solutions`), Tagline, and Portfolio explanation copy.
  - **Footer Settings Tab**: Edit Footer About Summary, ISO Certification Badge, Client Count Statistic, Copyright Notice, and Subtext Tagline.

### 4. Managing Header & Footer Menus
- Navigate to **Navigation**:
  - **Main Navigation**: Manage top header navigation links and active highlights.
  - **Footer Navigation**: Manage links rendered in the corporate footer.

### 5. Managing SEO & Social Meta Tags
- Navigate to **Collections** -> **Pages** (or **Projects**) -> Select an entry -> Click the **SEO & Social Meta** tab.
- Set custom Meta Title tags, Meta Descriptions for Google snippets, Open Graph image URLs, and Canonical links.

---

## 🎨 Design System & Technologies

- **CMS Framework**: Statamic v5 (Laravel-based Flat-File CMS)
- **CSS Framework**: Tailwind CSS v4 (`@tailwindcss/typography`)
- **Template Engine**: Statamic Antlers Template Engine
- **Typography**: *Plus Jakarta Sans* (Headings & Body) & *JetBrains Mono* (Code & Telemetry Badges)
- **Color Palette**: 
  - Background: Clean Slate (`bg-slate-50`)
  - Accent Colors: Indigo (`#6366f1`), Blue (`#2563eb`), & Emerald (`#10b981`)
  - Text: Dark Charcoal (`text-slate-900`) & Muted Slate (`text-slate-600`)

---

## 🚀 Local Development Setup

### Prerequisites
- PHP >= 8.2 with XAMPP or Herd
- Composer
- Node.js & npm

### Installation Steps

1. **Clone the repository**:
   ```bash
   cd e:/xampp/htdocs/statamic-demo
   ```

2. **Install PHP Dependencies**:
   ```bash
   composer install
   ```

3. **Install & Compile Frontend Assets**:
   ```bash
   npm install
   npm run dev
   ```

4. **Environment Setup**:
   Ensure `.env` contains your local application URL:
   ```env
   APP_URL=http://statamic-demo.test
   STATAMIC_STATIC_CACHING_STRATEGY=null
   STATAMIC_LICENSE_KEY=
   ```

5. **Run Development Server**:
   ```bash
   php artisan serve
   ```
   Or visit your local virtual host at `http://statamic-demo.test`.

6. **Clear Statamic Stache Cache** (if making direct flat-file modifications):
   ```bash
   php artisan statamic:stache:clear
   ```

---

## 📄 License & Attribution

Built for local testing, framework evaluation, and corporate portfolio demonstration. Powered by [Statamic](https://statamic.com) and [Tailwind CSS](https://tailwindcss.com).

---

<div align="center">

### Made with ❤️ by Nirav Gajera

**If you find this project useful, please consider giving it a ⭐ on GitHub!**

[↑ Back to Top](#-test-company---enterprise-it-industry-business-portfolio--statamic-demo)

</div>
