## Day 1: Setting Up Your Arsenal
* **The Goal:** Install and configure your core hacking tool.
* **The Tools:** 
  * **Burp Suite Community Edition** (Free web interception proxy).
  * **FoxyProxy** (Browser extension to route traffic easily into Burp).
* **Hands-On Action:**
  1. Download and install Burp Suite.
  2. Configure your browser to route traffic through `127.0.0.1:8080` using FoxyProxy.
  3. Install Burp’s CA certificate in your browser so you can inspect secure (HTTPS) traffic.
  4. Turn **Intercept On** in Burp, visit a website, and watch your browser's request pause inside Burp. Click **Forward** to let it load.

---

## Day 2: Mastering HTTP Requests & Responses
* **The Goal:** Understand how websites talk to servers (GET, POST, headers, parameters).
* **Free Resource:** PortSwigger Web Security Academy (create a free account).  
* **Hands-On Action:**
  1. Go to PortSwigger Academy and open their free lab for "HTTP basics" or just look at any login page.
  2. Capture a login request in Burp Suite. Identify:
     * **The Method:** Is it `GET` or `POST`?
     * **The Path:** E.g., `/login.php`.
     * **The Parameters:** E.g., `username=test&password=123`.
  3. Right-click the request in Burp and select **Send to Repeater**. Change a parameter value manually and hit **Send** to see how the server responds differently.

---

## Day 3: Hunting Your First Vulnerability (Reflected XSS)
* **The Goal:** Learn Cross-Site Scripting (XSS), one of the easiest beginner bugs to spot.
* **The Concept:** Finding a text box, search bar, or URL parameter where what you type gets printed right back onto the web page without safety checks.
* **Hands-On Action:**
  1. Go to PortSwigger Web Security Academy -> **Cross-Site Scripting (XSS)** -> complete the "Reflected XSS into HTML context with nothing encoded" lab.
  2. Find the search box in the lab, and type this exact payload: `<script>alert(1)</script>`
  3. If a pop-up box saying `1` appears, you have successfully executed XSS!

---

## Day 4: Leveling Up to Logic Flaws (IDOR)
* **The Goal:** Learn Insecure Direct Object Reference (IDOR)—the king of beginner bug bounty payouts.
* **The Concept:** When a website trusts user input blindly to fetch private files or profile IDs (e.g., `/account?id=101`).
* **Hands-On Action:**
  1. Go to PortSwigger Academy -> **Access Control** topic -> complete a free IDOR lab (e.g., viewing other users' profiles by changing an ID number).
  2. Practice changing numbers in URLs or request bodies using Burp Repeater to see if you can access data belonging to a different simulated user account.

---

## Day 5: Choosing Your Target & Reconnaissance
* **The Goal:** Pick a real, beginner-friendly public program on HackerOne.
* **Hands-On Action:**
  1. Log into your free HackerOne account and head to the **Directory / Hacktivity** page.
  2. Look for a small public program (avoid tech giants like Google/Meta). Read their policy rules carefully (check what features are in-scope).
  3. Create a normal account on that target web app, and spend 2 hours clicking every button while Burp Suite maps out all their endpoints, JavaScript files, and directories in the background.

---

## Day 6: Manual Testing Session
* **The Goal:** Apply what you learned on Days 3 and 4 to your chosen target.
* **Hands-On Action:**
  1. Test input forms and search boxes for XSS or input reflection.
  2. Look at every URL containing numbers or unique identifiers (like user profiles, shopping carts, or message IDs) and test for IDOR by swapping values.
  3. **Remember:** Only test features explicitly marked **In-Scope** in the program policy.

---

## Day 7: Writing a Professional Bug Report
* **The Goal:** Learn how to document and submit a finding correctly.
* **Hands-On Action:**
  1. Even if you haven't found a live bug yet (which is normal in week one), go to HackerOne's public **Hacktivity** page and read 5 disclosed reports submitted by other hackers.
  2. Notice the structure of a winning report:
     * **Title & Description:** Clear summary of the issue.
     * **Steps to Reproduce:** Step-by-step instructions so the triage team can easily recreate it.
     * **Impact:** What an attacker could achieve with this bug (e.g., "Allows an attacker to read arbitrary user profile data").
