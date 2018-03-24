# Project 7 - WordPress Pentesting

Time spent: **10** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress.

## Pentesting Report

### 1. WordPress <= 4.2 - Unauthenticated Stored Cross-Site Scripting (XSS)
  - [x] WPScan Vulnerability Database:
    - [7945](https://wpvulndb.com/vulnerabilities/7945)
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [x] Steps to recreate: 
    - https://klikki.fi/adv/wordpress2.html
  - [x] Affected source code:
    - N/A
  - [x] GIF Walkthrough: ![Imgur](https://imgur.com/w9Caf9x.gif)

### 2. WordPress <= 4.3 - Authenticated Shortcode Tags Cross-Site Scripting (XSS)
  - [x] WPScan Vulnerability Database:
    - [8186](https://wpvulndb.com/vulnerabilities/8186)
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.5
  - [x] Steps to recreate: 
    - https://blog.checkpoint.com/2015/09/15/finding-vulnerabilities-in-core-wordpress-a-bug-hunters-trilogy-part-iii-ultimatum/
  - [x] Affected source code:
    - N/A
  - [x] GIF Walkthrough: ![Imgur](https://imgur.com/kyL5SN9.gif)

### 3. WordPress 3.6.0-4.7.2 - Authenticated Cross-Site Scripting (XSS) via Media File Metadata
  - [x] WPScan Vulnerability Database:
    - [8765](https://wpvulndb.com/vulnerabilities/8765)
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [x] Steps to recreate: 
    - https://sumofpwn.nl/advisory/2016/wordpress_audio_playlist_functionality_is_affected_by_cross_site_scripting.html
    - http://seclists.org/oss-sec/2017/q1/563
  - [x] Affected source code:
    - [wp-admin/includes/media.php](https://github.com/WordPress/WordPress/commit/28f838ca3ee205b6f39cd2bf23eb4e5f52796bd7)
  - [x] GIF Walkthrough: ![Imgur](https://imgur.com/n6jZFok.gif)

### 4. WordPress 4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [x] WPScan Vulnerability Database:
    - [8768](https://wpvulndb.com/vulnerabilities/8768)
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [x] Steps to recreate: 
    - https://blog.sucuri.net/2017/03/stored-xss-in-wordpress-core.html
  - [x] Affected source code:
    - [wp-includes/embed.php](https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8)
  - [x] GIF Walkthrough: ![Imgur](https://imgur.com/kxZo8za.gif)

### 5. WordPress 3.3-4.7.4 - Large File Upload Error XSS
  - [x] WPScan Vulnerability Database:
    - [8819](https://wpvulndb.com/vulnerabilities/8819)
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.15
  - [x] Steps to recreate: 
    - https://hackerone.com/reports/203515
  - [x] Affected source code:
    - [wp-includes/js/plupload/handlers.js](https://github.com/WordPress/WordPress/commit/8c7ea71edbbffca5d9766b7bea7c7f3722ffafa6)
  - [x] GIF Walkthrough: ![Imgur](https://imgur.com/4BXE0E2.gif)

