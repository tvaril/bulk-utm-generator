# 🚀 Bulk UTM Generator

A powerful, client-side UTM link generator with automatic updates, data persistence, and export capabilities. Perfect for marketing teams managing multiple campaigns.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-GPL--v3-blue)
![Offline](https://img.shields.io/badge/works-offline-brightgreen)

### Key Points:
- ✅ **Freedom to use** - Use for any purpose
- ✅ **Freedom to study** - Access to source code
- ✅ **Freedom to modify** - Make changes as needed
- ✅ **Freedom to share** - Distribute copies
- ⚠️ **Copyleft** - Derivative works must also be GPL-licensed

## ✨ Features

- ✅ **Automatic UTM link generation** with live preview
- ✅ **Parameter sanitization** (lowercase, spaces→underscores)
- ✅ **URL validation** with automatic protocol completion
- ✅ **Proper handling** of anchors (#) and query parameters
- ✅ **Export to CSV and Excel**
- ✅ **QR code generation** with customizable settings
- ✅ **Data backup and restore** (JSON format)
- ✅ **Automatic/manual utm_id generation**
- ✅ **Autocomplete with history**
- ✅ **Advanced UTM parameters** (platform, format, tactic)
- ✅ **Quick fill** for empty rows
- ✅ **LocalStorage** with warning for issues
- ✅ **Browser compatibility check**
- ✅ **Offline indicator**
- ✅ **Complete help and tooltips**

## 📑 Table of Contents

- [How to Use](#how-to-use)
- [Required Fields](#required-fields)
- [Automatic Text Formatting](#automatic-text-formatting)
- [Automatic utm_id Generation](#automatic-utm_id-generation)
- [Optional Advanced Parameters](#optional-advanced-parameters)
- [Quick Fill](#quick-fill)
- [Export and Backup](#export-and-backup)
- [Data Storage](#data-storage)
- [QR Codes](#qr-codes)
- [Autocomplete](#autocomplete)
- [Data Management](#data-management)
- [Compatibility and Limitations](#compatibility-and-limitations)
- [Troubleshooting and Debugging](#troubleshooting-and-debugging)
- [Tips and Recommendations](#tips-and-recommendations)
- [Version History](#version-history)
- [Security and Limitations](#-security-and-limitations)

## How to Use

This tool helps you create tracked UTM links for your marketing campaigns. All data is stored locally in your browser.

### Getting Started

1. Open `index.html` in your browser
2. Fill in required fields (Base URL, utm_source, utm_medium, utm_campaign)
3. UTM link generates automatically
4. Copy or export your links

[⬆️ Back to top](#-table-of-contents)

## Required Fields

- **Base URL:** Enter the target address (e.g., `example.com` or `https://example.com/page`). The https:// protocol will be added automatically if not provided.
- **utm_source:** Traffic source (e.g., `facebook`, `google`, `newsletter`)
- **utm_medium:** Media type (e.g., `cpc`, `email`, `social`)
- **utm_campaign:** Campaign name (e.g., `summer_sale`, `black_friday`)

[⬆️ Back to top](#-table-of-contents)

## Automatic Text Formatting

All UTM parameters (except Base URL and utm_id) are automatically formatted:

- 🔤 **Convert to lowercase:** "FaceBook" → "facebook"
- 🔗 **Spaces → underscores:** "Summer Sale" → "summer_sale"
- 🧹 **Remove disallowed characters:** Only letters, numbers, hyphens (-) and underscores (_) are allowed

> 💡 **Note:** Changes take effect after you finish typing (Tab or Enter).

[⬆️ Back to top](#-table-of-contents)

## Automatic utm_id Generation

In the ⚙️ Settings section, you can enable/disable automatic `utm_id` generation:

- **✅ Enabled (default):** Generates ID in format `YYYYMMDD_XXX` (date + sequential number), e.g., `20240323_001`
- **✍️ Disabled:** You can enter custom ID manually

[⬆️ Back to top](#-table-of-contents)

## Optional Advanced Parameters

In the ⚙️ Settings section, you can show additional columns:

- **utm_source_platform:** Specific advertising platform (e.g., `facebook_ads`)
- **utm_creative_format:** Ad format (e.g., `video`, `banner`)
- **utm_marketing_tactic:** Campaign stage (e.g., `awareness`, `conversion`)

> ⚠️ **Important:** These parameters require custom setup in Google Analytics 4!

[⬆️ Back to top](#-table-of-contents)

## Quick Fill

Want to fill all empty rows with the same values? Use the **⚡ Quick fill** section above the table.

[⬆️ Back to top](#-table-of-contents)

## Export and Backup

- **💾 Export CSV:** Download your UTM links to CSV file *(works offline ✅)*
- **📊 Export Excel:** Download to XLSX format *(⚠️ requires internet)*
- **💼 Backup data (JSON):** Save complete backup including history *(works offline ✅)*
- **📥 Restore data (JSON):** Load previously saved backup *(works offline ✅)*

> 💡 **Tip:** If working without connection, use CSV export or JSON backup instead of Excel.

[⬆️ Back to top](#-table-of-contents)

## Data Storage

All data is automatically saved to your browser's **localStorage**:

- ✅ Data remains even after closing the browser
- ✅ Works offline
- ⚠️ Data is stored only in this browser
- 💡 We recommend creating regular backups (JSON)

[⬆️ Back to top](#-table-of-contents)

## QR Codes

For each generated UTM link, you can create a QR code with custom color settings, margin size, and error correction level. QR code can be downloaded in various formats (PNG, JPEG, SVG, EPS).

> ⚠️ **Important:** QR code generation requires internet connection (uses external API).

[⬆️ Back to top](#-table-of-contents)

## Autocomplete

When typing into fields, a history of previously used values is displayed. History is saved automatically and can be cleared in ⚙️ Settings → 💾 Data Management.

[⬆️ Back to top](#-table-of-contents)

## Data Management

- **🗑️ Clear rows:** Deletes all rows (preserves history and settings)
- **🧹 Clear autocomplete history:** Deletes only autocomplete history
- **🔄 Reset application:** Returns application to completely clean state *(⚠️ deletes EVERYTHING!)*

[⬆️ Back to top](#-table-of-contents)

## Compatibility and Limitations

### Supported Browsers

- **Recommended:** Chrome 90+, Firefox 88+, Edge 90+, Safari 14+
- **Minimum:** Chrome 49+, Firefox 45+, Edge 14+, Safari 10+
- ❌ **Not supported:** Internet Explorer (any version)

### Features Requiring Internet

- **📊 Excel export:** Requires loading external SheetJS library from CDN
- **📱 QR codes:** Use online API for generation (api.qrserver.com)

### What Happens with Problems

- **Old browser:** Red warning at top with problem description
- **Lost connection:** Orange warning and notice about limited features
- **Full localStorage:** Warning and recommendation to create backup
- **Unsupported localStorage:** Data won't be saved between sessions

### What Always Works (Even Offline)

- ✅ UTM link generation
- ✅ URL validation and cleaning
- ✅ UTM parameter sanitization
- ✅ CSV export
- ✅ Saving to localStorage (if supported)
- ✅ JSON backup and restore
- ✅ Autocomplete and history

[⬆️ Back to top](#-table-of-contents)

## Troubleshooting and Debugging

### Developer Console

All technical information, verifications, and error messages are logged to the **browser console**. This is useful for diagnosing problems.

### How to Open Console

**Windows/Linux:**
- `F12`
- `Ctrl + Shift + I`
- `Ctrl + Shift + J`
- Right-click → Inspect → Console

**macOS:**
- `Cmd + Option + I`
- `Cmd + Option + J`
- Right-click → Inspect Element → Console

### What You'll Find in Console

- ✅ **Version info:** `🚀 UTM Generator v1.0.0`
- ✅ **Compatibility check:** "Browser compatibility check passed!"
- ✅ **Backup info:** "Restoring backup from version..."
- ⚠️ **Warnings:** localStorage issues, different backup versions, etc.
- ❌ **Errors:** Detailed information about URL parsing problems, validation, etc.
- 📝 **Debug logs:** Technical information about application operation

### Common Problems and Solutions

<details>
<summary><strong>❌ Data isn't saving or backup won't load</strong></summary>

**Possible causes:**
- LocalStorage is full or blocked
- Using private mode (Incognito)
- Browser blocks localStorage for local files

**Solutions:**
- Open console (F12) and look for red errors
- Check if orange warning displays at top
- Clear browser data or use different browser
- Use JSON backups for data transfer
</details>

<details>
<summary><strong>❌ URL not generating or error message during validation</strong></summary>

**Possible causes:**
- Invalid URL format (missing domain or TLD)
- Disallowed protocol (ftp://, javascript:, etc.)
- Special characters in URL

**Solutions:**
- Open console and check warnings related to URL
- Make sure URL contains domain with TLD (e.g., `example.com`)
- Protocol https:// will be added automatically if missing
- Console will show: "Could not parse URL for cleaning: ..."
</details>

<details>
<summary><strong>❌ QR code or Excel export not working</strong></summary>

**Possible causes:**
- You are offline (no internet connection)
- External API or library failed to load
- Third-party blocking (AdBlock, firewall)

**Solutions:**
- Check internet connection
- Look for red errors in console (e.g., "Failed to load resource")
- Temporarily disable AdBlock or other extensions
- Use CSV export (works offline) instead of Excel
</details>

<details>
<summary><strong>❌ Application is slow or not responding</strong></summary>

**Possible causes:**
- Too many rows (hundreds)
- Large autocomplete history
- Full localStorage

**Solutions:**
- Export data and delete old rows
- Clear autocomplete history (⚙️ Settings → Clear history)
- Create backup and reset application
- In console you can check data size: `localStorage`
</details>

### Debugging Tips

- 🔴 **Red messages** = critical errors that stop function
- 🟡 **Yellow messages** = warnings, application works but something isn't ideal
- ⚪ **Regular messages** = information about progress (loading, saving, etc.)
- When reporting problems, **always attach console screenshot**
- Text from console can be copied (right-click → Copy message)

[⬆️ Back to top](#-table-of-contents)

## 🔒 Security and Limitations

> ⚠️ **IMPORTANT SECURITY NOTICE**

This application is **not designed for public internet deployment** and does not include advanced security mechanisms such as protection against XSS attacks, CSRF attacks, or input sanitization for online environments.

### 🎯 Intended Use

The application is primarily designed for:

- ✅ **Local use** - Running directly from your computer (`file://` protocol)
- ✅ **Internal corporate environment** - Intranet behind firewall
- ✅ **Personal projects** - Individuals or small teams
- ✅ **Offline work** - No internet connection required

### ⚠️ Security Limitations

The application **does not include** the following security features:

- ❌ Protection against XSS (Cross-Site Scripting) attacks
- ❌ Protection against CSRF (Cross-Site Request Forgery)
- ❌ Server-side validation and data sanitization
- ❌ User authentication and authorization
- ❌ Rate limiting for API requests
- ❌ Sensitive data encryption
- ❌ Content Security Policy (CSP) headers

### 🛡️ Recommendations for Safe Use

- ✅ **Use locally** - Open HTML file directly in your browser
- ✅ **Don't share sensitive data** - Avoid using for confidential campaigns on public internet
- ✅ **Backup regularly** - Data is stored only in browser localStorage
- ✅ **Trust only your own backups** - Don't load JSON backups from unknown sources
- ✅ **Use in controlled environments** - Behind firewall or on trusted networks only

### 💡 For Production Deployment

If you plan to deploy this application on a public web server, we **strongly recommend**:

1. Implement server-side validation
2. Add Content Security Policy (CSP)
3. Sanitize all inputs on server side
4. Use HTTPS with valid certificates
5. Implement user authentication and authorization
6. Add rate limiting for API endpoints
7. Regular security audits and penetration testing
8. Monitor for suspicious activity
9. Keep dependencies updated
10. Follow OWASP security guidelines

### 📚 Further Reading

- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [Content Security Policy Guide](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP)
- [XSS Prevention Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html)

[⬆️ Back to top](#-table-of-contents)

## Tips and Recommendations

- ✅ Use **consistent naming** across campaigns
- ✅ Write values in **lowercase** without diacritics
- ✅ Use **underscores** instead of spaces (happens automatically)
- ✅ For long-term campaigns use **utm_id** for better tracking
- ✅ Regularly **backup your data** to JSON file

[⬆️ Back to top](#-table-of-contents)

## Version History

### v1.0.0 (January 31, 2025) - Stable version

Initial release with complete feature set.

[⬆️ Back to top](#-table-of-contents)

## 📄 License

MIT License - feel free to use and modify for your needs.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

## 👨‍💻 Author

Created for efficient UTM campaign management.

### 🙏 Acknowledgments
[SheetJS](https://sheetjs.com/) for Excel export functionality
[QR Server](https://goqr.me/) API for QR code generation
[Gemini Pro 2.5](https://gemini.google.com/?hl=cs)
[Claude Sonet 4.5](https://claude.ai/)
All contributors and testers

---

**Made with ❤️ for marketers**
