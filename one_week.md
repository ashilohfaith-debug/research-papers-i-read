https://www.youtube.com/watch?v=Opn3lAURnF8

## Day 1: Setting Up Your Arsenal
* **The Goal:** Install and configure Burp Suite and your browser proxy.
* **The Tools:** 
  * **Burp Suite Community Edition** (Free interception proxy).
  * **FoxyProxy** (Browser extension).
* **Hands-On Action:**
  1. Install Burp Suite and configure your browser to route traffic through `127.0.0.1:8080` using FoxyProxy.
  2. Install Burp’s CA certificate in your browser so you can inspect HTTPS traffic.
  3. Turn **Intercept On** in Burp, visit a website, and verify that you can pause, view, and forward web traffic.

---

## Day 2: Understanding HTTP & Redirect Parameters
* **The Goal:** Learn how websites handle page routing and user navigation using parameters.
* **Free Resource:** PortSwigger Web Security Academy (create a free account).  
* **Hands-On Action:**
  1. Log into a web app or lab environment and trigger a login or logout action.
  2. Capture the request in Burp Suite and look for parameters controlling where the user goes next (e.g., `?returnPath=`, `?next=`, `?url=`).
  3. Send the request to Burp Repeater, modify the redirection parameter value, and observe how the server reacts.

---

## Day 3: Mastering Open Redirect Mechanics
* **The Goal:** Learn how open redirect vulnerabilities happen and how to spot them manually.
* **The Concept:** Testing if an application blindly accepts an external URL in a redirection parameter.
* **Hands-On Action:**
  1. Find a parameter designated for redirection (e.g., `url=https://internal-site.com`).
  2. Swap out the internal URL with an external domain (e.g., `https://www.google.com`).
  3. Check if the application redirects your browser straight to the external site without warning.

---

## Day 4: Practicing Filter Bypasses
* **The Goal:** Learn how developers try to block open redirects and how to bypass those defenses.
* **The Concept:** Bypassing weak regular expressions or filters that look for specific strings.
* **Hands-On Action:**
  1. Test common bypass variations if a basic external URL is blocked:
     * Protocol-relative URLs: `//google.com`
     * Backslash tricks: `/\google.com`
     * Using an `@` symbol or subdomain prefix trick.
  2. Test these variations inside a local lab environment or a practice lab to see which inputs trick the server into redirecting anyway.

---

## Day 5: Setting Up a Local Lab & Testing Ground
* **The Goal:** Practice open redirect hunting safely in a controlled environment.
* **Hands-On Action:**
  1. Set up a local test environment like **DVWA (Damn Vulnerable Web Application)** via XAMPP or Docker, which features pre-built vulnerable redirection scripts.
  2. Alternatively, use the free **PortSwigger Web Security Academy** labs dedicated to open redirection.
  3. Spend 2 hours intentionally breaking and exploiting redirection flows in the local environment.

---

## Day 6: Recon on Target Platforms
* **The Goal:** Look for redirection parameters in real-world applications or public bug bounty targets.
* **Hands-On Action:**
  1. Open a beginner-friendly public program scope on HackerOne.
  2. Browse features that require redirection—such as login pages, single sign-on (SSO) flows, language switchers, or "back to safety" buttons.
  3. Map out every parameter handling paths or URLs using Burp Suite's proxy history.

---

## Day 7: Documenting and Reporting Open Redirects
* **The Goal:** Learn how to write a clear, professional report for an open redirect finding.
* **Hands-On Action:**
  1. Review how other researchers report open redirects by looking at public disclosures on HackerOne's Hacktivity.
  2. Draft a mock report detailing:
     * **Vulnerable Endpoint:** Exact URL and parameter.
     * **Proof of Concept:** Step-by-step reproduction instructions showing the crafted malicious link.
     * **Impact:** Explaining how an attacker could leverage the redirect for phishing or chaining into other bugs.
