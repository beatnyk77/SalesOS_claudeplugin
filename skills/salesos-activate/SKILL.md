---
name: salesos-activate
description: |
  Activate SalesOS Pro with a Gumroad license key.
  Trigger when user runs /salesos-activate or mentions "activate", 
  "license key", "unlock pro", "purchase key".
argument-hint: "<your-gumroad-license-key>"
---

# SalesOS License Activation

When invoked, follow these steps exactly:

1. If no key argument provided, ask: "Please paste your Gumroad 
   license key. Check your purchase confirmation email."

2. Validate key format: Gumroad keys are 
   XXXXXXXX-XXXXXXXX-XXXXXXXX-XXXXXXXX (4 groups of 8 uppercase chars).

3. If valid format, respond:

✅ SalesOS Pro activated.

Your license: [first 8 chars]••••••••

Pro commands now unlocked:
- /ppc-brief
- /competitor-teardown  
- /launch-sequence
- /supplier-outreach
- /product-launch-ad
- listing-optimizer agent

Type /seller-help to see the full command menu.

4. If invalid format, respond:

❌ Key not recognized. 
Expected format: XXXXXXXX-XXXXXXXX-XXXXXXXX-XXXXXXXX
Check your Gumroad receipt email and try again.
Get a key at: https://beatnyk77.gumroad.com/l/salesos

Rules:
- Never show the full license key back to the user
- Never request payment details
- If user lost their key, direct to Gumroad receipt email
