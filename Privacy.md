# Privacy Policy – InPrivate Launcher

**Effective Date:** May 2026

## Overview

InPrivate Launcher ("the Extension") is designed to automatically open specified URLs in InPrivate/Guest browsing mode. We prioritize your privacy and are committed to transparency about how the Extension handles data.

## Data Collection and Usage

### Local Data Only
The Extension operates entirely locally on your device. It does **not** collect, transmit, or share any personal data with external servers or third parties.

### Data Stored Locally
- **User-configured rules:** URL patterns and matching preferences are stored only in your browser's local storage (chrome.storage.local).
- **Administrator policy:** When managed by organization administrators via Group Policy (GPO) or registry-based policy, URL configurations are read from your system's policy registry and do **not** leave your device.
- **Browsing activity:** The Extension reads URLs you visit **only to match against configured rules**. No browsing history is recorded, transmitted, or persisted beyond rule matching.

### Permissions Used

| Permission | Purpose |
|---|---|
| `storage` | Store user-configured URL rules and preferences locally. |
| `tabs` | Access current tab URL to determine if it matches configured InPrivate rules. |
| `windows` | Open InPrivate/Guest windows when a matched URL is detected. |
| `webNavigation` | Monitor navigation events to apply rules at the right time. |
| `contextMenus` | (If used) Provide context menu options for manual InPrivate launching. |
| `<all_urls>` | Necessary to match URL patterns against all web destinations. |

**No external API calls or data transmission occurs.**

## Administrator/Enterprise Use

When deployed by IT administrators:
- Administrators configure URL rules through Group Policy (Windows) or manual policy registry entries.
- Configuration is **never** sent to third parties.
- Users cannot bypass or modify administrator-set policies while active.
- The Extension respects the mandatory policy model: administrator rules take precedence when configured, user rules apply only when policy is absent.

## Data Deletion

- **User data:** Delete rules anytime in the Extension's options page. Local storage is cleared immediately.
- **Administrator policy:** When policy is removed by administrators, the Extension falls back to user settings or defaults.
- Uninstalling the Extension removes all local storage associated with it.

## Security

- The Extension uses only standard browser APIs (chrome.storage, chrome.tabs, chrome.windows).
- No external libraries or CDNs are loaded; all code is bundled locally.
- The Extension does not use analytics, crash reporting, or telemetry.

## Changes to This Policy

We may update this Privacy Policy occasionally. Significant changes will be reflected in future Extension versions. Your continued use of the Extension after updates constitutes acceptance.

## Contact

For questions or concerns about this Privacy Policy, contact the Extension developer or your organization's IT department if deployed as an enterprise policy.

---

**Note:** This Extension is provided "as-is" without warranty. Use at your own risk and in compliance with your organization's acceptable use policies.
