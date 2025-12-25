# radical_highlighter

# Injecting JavaScript into a Website (Chrome)

This document explains common ways to inject custom JavaScript into websites using **Chrome**, without modifying the site’s source code. Typical use cases include automation, UI tweaks, learning/debugging, and personal productivity scripts.

---

## 1. User Script (Tampermonkey / UserJS)

### What it is
A **userscript** runs automatically on matching websites after the page loads.  
Tampermonkey is the most popular userscript manager for Chrome.

### When to use
- Persistent scripts
- Run on specific domains or pages
- Need access to page context and DOM
- Want easy enable/disable

### Steps
1. Install **Tampermonkey** from Chrome Web Store
2. Create a new script
3. Add metadata and JavaScript code

### Example
```javascript
// ==UserScript==
// @name         Example Injector
// @namespace    https://example.com
// @version      1.0
// @description  Inject custom JS into a site
// @match        https://example.com/*
// @grant        none
// ==/UserScript==

(function () {
  'use strict';
  console.log('Injected via Tampermonkey');
})();
