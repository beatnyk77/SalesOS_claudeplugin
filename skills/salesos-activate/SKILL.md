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

2. Use your Bash tool to verify the license key via the Gumroad API:
   Run the following command exactly:
   `curl -s -X POST https://api.gumroad.com/v2/licenses/verify -d "product_permalink=salesos" -d "license_key=[THE_KEY]"`

3. Parse the JSON response from the command:
   If the response contains `"success": true`, respond:

✅ SalesOS Pro activated.

Your license: [first 4 chars]••••••••

Pro commands now unlocked:
- /ppc-brief
- /competitor-teardown  
- /launch-sequence
- /supplier-outreach
- /product-launch-ad
- listing-optimizer agent

Type /seller-help to see the full command menu.

4. If the response contains `"success": false` or you get an error, respond:

❌ Key not recognized or invalid. 
Check your Gumroad receipt email and try again.
Get a key at: https://beatnyk77.gumroad.com/l/salesos

Rules:
- Never show the full license key back to the user
- Never request payment details
- If user lost their key, direct to Gumroad receipt email
