# Security policy

## Never publish

- API keys, bearer tokens, OAuth grants, cookies, or session data.
- Real Make connection identifiers, Google Drive folder identifiers, or Notion database/data-source identifiers.
- Private email addresses, personal photos, EXIF metadata, or Drive file URLs.
- Unredacted Make exports, execution logs, or API responses.

## Before each commit

1. Review each file for credentials, emails, IDs, and personal data.
2. Search for `sk-`, `Bearer`, `api_key`, `token`, `secret`, `password`, and resource identifiers.
3. Confirm the public blueprint contains only placeholders.
4. Keep all photos and private configuration outside the repository.
5. If credentials are exposed, revoke or rotate them immediately; deleting a file alone does not remove it from Git history.

This repository contains a deliberately non-operational, sanitized Make example.
