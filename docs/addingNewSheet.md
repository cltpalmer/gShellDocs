# 🔥 gShell Quick Checklist: Add New Tab or New Google Sheet

Use this guide to quickly integrate new Google Sheets tabs or entirely new Google Sheets with different service accounts into your gShell CLI.

---

## ✅ Checklist: Add New Tab to SAME Sheet / SAME Service Key

*Example: You added a tab called `Stats` to an existing sheet that uses `gShellServiceKey.json`*

1. 🔐 **Ensure the new tab is inside the same shared Google Sheet**
2. 🧠 **Note the exact tab name** (case-sensitive, e.g., `Stats`, `Integrations`, etc.)
3. 📍 **Define the range** you want to fetch from (e.g., `Stats!A1:D20`)
4. 🧾 **Add a new entry to `commands.json`:**

## JSON Example
"getStatsData": {
  "label": "📈 Stats",
  "endpoint": "http://localhost:3001/read?account=main&sheetId=YOUR_SHEET_ID&range=Stats!A1:D20"
}

## Test it in gShell: type `getStatsData`
