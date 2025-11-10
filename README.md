# 🚀 UTM Generator

A fast, offline-first, single-page UTM link generator with automatic updates, QR code generation, and data persistence. This tool is a single HTML file with no external dependencies (except for optional Excel export and QR generation APIs).



## 📑 Table of Contents

1.  [Version and Changelog](#version-and-changelog)
2.  [How to Use UTM Generator](#how-to-use-utm-generator)
3.  [Required Fields](#required-fields)
4.  [Automatic Text Formatting](#automatic-text-formatting)
5.  [Automatic utm_id Generation](#automatic-utm_id-generation)
6.  [Optional Advanced Parameters](#optional-advanced-parameters)
7.  [Quick Fill](#quick-fill)
8.  [Export and Backup](#export-and-backup)
9.  [Data Storage](#data-storage)
10. [QR Codes](#qr-codes)
11. [Autocomplete](#autocomplete)
12. [Data Management](#data-management)
13. [Compatibility and Limitations](#compatibility-and-limitations)
14. [Troubleshooting and Debugging](#troubleshooting-and-debugging)
15. [Tips and Recommendations](#tips-and-recommendations)

---

## 📋 Version and Changelog
<a id="help-version"></a>

**Current Version:** 1.0.0 (Jan 31, 2025)

<details>
<summary>📜 Show Version History</summary>

#### v1.0.0 (Jan 31, 2025) - Stable Version
* ✅ Automatic UTM link generation with live preview
* ✅ Parameter sanitization (lowercase, spaces→underscores)
* ✅ URL validation with automatic protocol addition
* ✅ Correct handling of anchors (#) and query parameters
* ✅ Export to CSV and Excel
* ✅ QR code generation with settings
* ✅ Data backup and restore (JSON)
* ✅ Automatic/manual utm_id generation
* ✅ Autocomplete with history
* ✅ Advanced UTM parameters (platform, format, tactic)
* ✅ Quick fill for empty rows
* ✅ LocalStorage with warnings on issues
* ✅ Browser compatibility check
* ✅ Offline indicator
* ✅ Complete help and tooltips

</details>

---

## 🎯 How to Use UTM Generator
<a id="help-how-to-use"></a>

This tool helps you create tracked UTM links for your marketing campaigns. All data is saved locally in your browser.

---

## 📋 Required Fields
<a id="help-required-fields"></a>

* **Base URL:** Enter the destination address (e.g., `example.com` or `https://example.com/page`). The https:// protocol is added automatically if you omit it.
* **utm_source:** Traffic source (e.g., `facebook`, `google`, `newsletter`)
* **utm_medium:** Medium type (e.g., `cpc`, `email`, `social`)
* **utm_campaign:** Campaign name (e.g., `summer_sale`, `black_friday`)

---

## ✏️ Automatic Text Formatting
<a id="help-auto-formatting"></a>

All UTM parameters (except Base URL and utm_id) are automatically formatted:

* 🔤 **Converted to lowercase:** "FaceBook" → "facebook"
* 🔗 **Spaces → underscores:** "Summer Sale" → "summer_sale"
* 🧹 **Removal of disallowed characters:** Only letters, numbers, hyphens (-), and underscores (_) are allowed

> **💡 Note:** Changes take effect after you finish typing (Tab or Enter).

---

## 🔢 Automatic utm_id Generation
<a id="help-utm-id"></a>

In the ⚙️ Settings section, you can enable/disable automatic `utm_id` generation:

* **✅ Enabled (default):** Generates an ID in the format `YYYYMMDD_XXX` (date + sequence number), e.g., `20240323_001`
* **✍️ Disabled:** You can enter your own custom ID manually

---

## ➕ Optional Advanced Parameters
<a id="help-advanced-params"></a>

In the ⚙️ Settings section, you can show additional columns:

* **utm_source_platform:** Specific advertising platform (e.g., `facebook_ads`)
* **utm_creative_format:** Ad format (e.g., `video`, `banner`)
* **utm_marketing_tactic:** Campaign phase (e.g., `awareness`, `conversion`)

> **⚠️ Important:** These parameters require custom setup in Google Analytics 4!

---

## ⚡ Quick Fill
<a id="help-quick-fill"></a>

Want to fill all empty rows with the same values? Use the **⚡ Quick Fill** section above the table.

---

## 📤 Export and Backup
<a id="help-export"></a>

* **💾 Export CSV:** Download your UTM links to a CSV file (works offline ✅)
* **📊 Export Excel:** Download in XLSX format (⚠️ requires internet)
* **💼 Backup Data (JSON):** Save a complete backup including history (works offline ✅)
* **📥 Restore Data (JSON):** Load a previously saved backup (works offline ✅)

> **💡 Tip:** If you are working offline, use CSV export or JSON backup instead of Excel.

---

## 🗂️ Data Storage
<a id="help-storage"></a>

All data is automatically saved to your browser's **localStorage**:

* ✅ Data persists even after closing the browser
* ✅ Works offline
* ⚠️ Data is stored *only* in this browser
* 💡 We recommend creating regular backups (JSON)

---

## 📱 QR Codes
<a id="help-qr"></a>

For each generated UTM link, you can create a QR code with custom settings for colors, margin size, and error correction level. You can download the QR code in various formats (PNG, JPEG, SVG, EPS).

> **⚠️ Important:** QR code generation requires an internet connection (uses an external API).

---

## 🔍 Autocomplete
<a id="help-autocomplete"></a>

When typing in fields, a history of previously used values is displayed. The history is saved automatically and can be cleared in ⚙️ Settings → 💾 Data Management.

---

## 🛠️ Data Management
<a id="help-data-management"></a>

* **🗑️ Clear Rows:** Deletes all rows (keeps history and settings)
* **🧹 Clear Autocomplete History:** Deletes only the autocomplete history
* **🔄 Reset Application:** Resets the application to a completely clean state (⚠️ deletes EVERYTHING!)

---

## ⚠️ Compatibility and Limitations
<a id="help-compatibility"></a>

### 📱 Supported Browsers
* **Recommended:** Chrome 90+, Firefox 88+, Edge 90+, Safari 14+
* **Minimum:** Chrome 49+, Firefox 45+, Edge 14+, Safari 10+
* ❌ **Not Supported:** Internet Explorer (any version)

### 🌐 Features Requiring Internet
* **📊 Export to Excel:** Requires loading the external SheetJS library from a CDN
* **📱 QR Codes:** Use an online API for generation (api.qrserver.com)

### 🔒 What Happens When Problems Occur
* **Old Browser:** Red warning at the top with a description of the problem
* **Lost Connection:** Orange warning and notification of limited functionality
* **Full localStorage:** Warning and recommendation to create a backup
* **Unsupported localStorage:** Data will not be saved between sessions

### 🛡️ What Always Works (Even Offline)
* ✅ UTM link generation
* ✅ URL validation and cleaning
* ✅ UTM parameter sanitization
* ✅ Export to CSV
* ✅ Saving to localStorage (if supported)
* ✅ JSON backup and restore
* ✅ Autocomplete and history

---

## 🔧 Troubleshooting and Debugging
<a id="help-debugging"></a>

### 📊 Developer Console
All technical information, verifications, and error messages are logged to the **browser console**. This is useful for diagnosing problems.

### 🖥️ How to Open the Console

**🪟 Windows/Linux:**
* `F12`
* `Ctrl + Shift + I`
* `Ctrl + Shift + J`
* Right-click → Inspect → Console

**🍎 macOS:**
* `Cmd + Option + I`
* `Cmd + Option + J`
* Right-click → Inspect Element → Console

### 🔍 What You'll Find in the Console
* ✅ **Version Info:** `🚀 UTM Generator v1.0.0`
* ✅ **Compatibility Check:** "Browser compatibility check passed!"
* ✅ **Backup Info:** "Restoring backup from version..."
* ⚠️ **Warnings:** Problems with localStorage, different backup versions, etc.
* ❌ **Errors:** Detailed information about problems parsing URLs, validation, etc.
* 📝 **Debug Logs:** Technical information about the application's runtime

### 🛠️ Common Problems and Solutions

<details>
<summary>❌ Data is not saving or backup is not loading</summary>

<p><strong>Possible Causes:</strong></p>
<ul>
<li>LocalStorage is full or blocked</li>
<li>You are using private mode (Incognito)</li>
<li>The browser is blocking localStorage for local files</li>
</ul>
<p><strong>Solution:</strong></p>
<ul>
<li>Open the console (F12) and look for red errors</li>
<li>Check if an orange warning is displayed at the top</li>
<li>Clear browser data or use a different browser</li>
<li>Use JSON backups to transfer data</li>
</ul>

</details>

<details>
<summary>❌ URL is not generating or validation error message</summary>

<p><strong>Possible Causes:</strong></p>
<ul>
<li>Invalid URL format (missing domain or TLD)</li>
<li>Disallowed protocol (ftp://, javascript:, etc.)</li>
<li>Special characters in the URL</li>
</ul>
<p><strong>Solution:</strong></p>
<ul>
<li>Open the console and check for URL-related warnings</li>
<li>Ensure the URL includes a domain with a TLD (e.g., <code>example.com</code>)</li>
<li>The https:// protocol is added automatically if missing</li>
<li>The console will show: "Could not parse URL for cleaning: ..."</li>
</ul>

</details>

<details>
<summary>❌ QR code or Excel export is not working</summary>

<p><strong>Possible Causes:</strong></p>
<ul>
<li>You are offline (no internet connection)</li>
<li>The external API or library failed to load</li>
<li>Third-party blocking (AdBlock, firewall)</li>
</ul>
<p><strong>Solution:</strong></p>
<ul>
<li>Check your internet connection</li>
<li>Look in the console for red errors (e.g., "Failed to load resource")</li>
<li>Temporarily disable AdBlock or other extensions</li>
<li>Use CSV export (works offline) instead of Excel</li>
</ul>

</details>

<details>
<summary>❌ Application is slow or unresponsive</summary>

<p><strong>Possible Causes:</strong></p>
<ul>
<li>Too many rows (hundreds)</li>
<li>Large autocomplete history</li>
<li>Full localStorage</li>
</ul>
<p><strong>Solution:</strong></p>
<ul>
<li>Export your data and delete old rows</li>
<li>Clear the autocomplete history (⚙️ Settings → Clear History)</li>
<li>Create a backup and reset the application</li>
<li>You can check data size in the console: <code>localStorage</code></li>
</ul>

</details>

### 💡 Debugging Tips
* 🔴 **Red messages** = critical errors that stop functionality
* 🟡 **Yellow messages** = warnings, the app works, but something is not ideal
* ⚪ **Regular messages** = information about progress (loading, saving, etc.)
* If you report a problem, **always include a screenshot of the console**
* You can copy text from the console (Right-click → Copy message)

---

## 💡 Tips and Recommendations
<a id="help-tips"></a>

* ✅ Use **consistent naming** across campaigns
* ✅ Write values in **lowercase** without diacritics
* ✅ Use **underscores** instead of spaces (happens automatically)
* ✅ For long-term campaigns, use **utm_id** for better tracking
* ✅ Regularly **back up your data** to a JSON file