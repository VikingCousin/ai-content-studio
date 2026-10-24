# AI Content Studio

AI-assisted photo editing workflow for vertical social-media stories, built with Make, Google Drive, Notion, CloudConvert, and OpenAI.

> **Public documentation and sanitized template only.** This repository does not contain the live Make scenario, API credentials, personal photos, or private Notion data.

## Workflow

1. Watch an input folder in Google Drive for new photos.
2. Download the original photo.
3. Convert unsupported HEIC photos to JPEG using CloudConvert.
4. Analyze the image with OpenAI Vision.
5. Retrieve candidate editing prompts from Notion.
6. Select a suitable style with an OpenAI text model.
7. Edit the photo with GPT Image 1.5, prioritizing identity preservation.
8. Upload the result to a Google Drive approval folder for manual review.

The workflow is configured in Make, not hosted or executed by GitHub. No automatic posting, captions, or hashtags.

## Repository contents

- `blueprints/make-scenario.public-template.json` — **sanitized, older example** of the initial five-module scenario; not the current live configuration and not ready to activate.
- `docs/architecture.md` — architecture, differences from the example, and implementation considerations.
- `docs/security.md` — publication and secrets policy.
- `.env.example` — placeholder variable names only.
- `.gitignore` — excludes photos, credentials, logs, and private exports.

## Security

Never commit actual Make blueprint exports without reviewing and redacting connection IDs, folder IDs, data-source IDs, personal information, and credentials. Keep API keys in service-managed connections or secret stores.

## Status

The live Make workflow has been manually tested, but the sanitized example in this repository is intentionally incomplete. Operational behavior, error handling, daily scheduling, HEIC support, and identity consistency must be validated independently in your Make account.
