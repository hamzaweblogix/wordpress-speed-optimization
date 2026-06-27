# ⚡ WordPress Speed Optimisation — 40 → 90+ PageSpeed

[![WordPress](https://img.shields.io/badge/WordPress-Performance-21759B?style=flat-square&logo=wordpress&logoColor=white)](https://wordpress.org)
[![PageSpeed](https://img.shields.io/badge/PageSpeed-40_→_90%2B-success?style=flat-square&logo=googlechrome&logoColor=white)](https://pagespeed.web.dev)
[![Core Web Vitals](https://img.shields.io/badge/Core_Web_Vitals-Optimised-4285F4?style=flat-square&logo=google&logoColor=white)](https://web.dev/vitals/)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)

> A battle-tested WordPress speed optimisation workflow that consistently pushes sites from **40 → 90+ PageSpeed score**. Includes configs, checklists, and ready-to-use code snippets.

---

## 📋 Overview

This repo documents the exact workflow I use on every client project to dramatically improve WordPress performance. Not theory — these are the actual steps, configs, and code I use to get real results.

**Typical results:**
- PageSpeed Mobile: 40s → 85–92
- PageSpeed Desktop: 55s → 92–98
- Largest Contentful Paint: 8s → under 2.5s
- Total Blocking Time: 600ms → under 100ms

---

## 🎯 Optimisation Checklist

### Phase 1 — Hosting & Server
- [ ] Move to LiteSpeed or Nginx server (avoid Apache shared hosting)
- [ ] Enable HTTP/2 or HTTP/3
- [ ] Use a server-level object cache (Redis/Memcached)
- [ ] Enable Gzip/Brotli compression
- [ ] Set up PHP 8.x

### Phase 2 — Caching
- [ ] Install LiteSpeed Cache (or WP Rocket on non-LiteSpeed)
- [ ] Enable page caching
- [ ] Enable browser caching (1 year for static assets)
- [ ] Enable object caching
- [ ] Enable database query caching

### Phase 3 — Images
- [ ] Convert all images to WebP
- [ ] Add lazy loading to below-fold images
- [ ] Set explicit width/height on all images (prevents CLS)
- [ ] Use a CDN for image delivery (Cloudflare or BunnyCDN)
- [ ] Compress images with ShortPixel or Smush

### Phase 4 — CSS & JavaScript
- [ ] Remove unused CSS (PurgeCSS or plugin)
- [ ] Defer non-critical JavaScript
- [ ] Minify CSS, JS, and HTML
- [ ] Eliminate render-blocking resources
- [ ] Load Google Fonts locally (no external request)

### Phase 5 — Database
- [ ] Remove post revisions (keep max 3)
- [ ] Delete transients and expired data
- [ ] Optimise database tables (WP-Optimize)
- [ ] Remove unused plugins

### Phase 6 — Core Web Vitals
- [ ] LCP under 2.5s (preload hero image)
- [ ] CLS under 0.1 (set image dimensions)
- [ ] FID/INP under 100ms (reduce JS)
- [ ] TTFB under 800ms (caching + server)

---

## 📁 Files Included

```
├── configs/
│   ├── nginx.conf              # Optimised Nginx config
│   ├── .htaccess               # Apache caching & compression rules
│   ├── wp-config-additions.php # WordPress performance constants
│   └── litespeed-cache.ini     # LiteSpeed Cache settings export
├── snippets/
│   ├── disable-emojis.php      # Remove emoji scripts
│   ├── local-google-fonts.php  # Self-host Google Fonts
│   ├── remove-query-strings.php
│   └── preload-hero-image.php
└── checklist.md                # Full optimisation checklist
```

---

## 🛠️ Quick Wins (5 Minutes or Less)

```php
// Add to wp-config.php for immediate performance boost
define('WP_POST_REVISIONS', 3);
define('AUTOSAVE_INTERVAL', 300);
define('WP_CACHE', true);
define('COMPRESS_SCRIPTS', true);
define('COMPRESS_CSS', true);
```

---

## 📊 Before & After Results

| Metric | Before | After |
|--------|--------|-------|
| PageSpeed Mobile | ~40 | 90+ |
| PageSpeed Desktop | ~55 | 95+ |
| Page Load Time | 6–8s | Under 2s |
| Page Size | 3–5 MB | Under 1 MB |
| Requests | 80–120 | 30–50 |

---

## 🤝 Need This Done For Your Site?

I offer WordPress speed optimisation as a standalone service — guaranteed to improve your PageSpeed score.

[![Hire on Upwork](https://img.shields.io/badge/Hire_Me_on_Upwork-6fda44?style=for-the-badge&logo=upwork&logoColor=white)](https://www.upwork.com/freelancers/~0107e870033e421590)
[![View Profile](https://img.shields.io/badge/GitHub_Profile-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/hamzaweblogix)

---

## 📄 License

MIT — use freely on client and personal projects.
