# Architecture

## Intended live workflow

Google Drive (watch new files) → Google Drive (download) → CloudConvert (HEIC → JPG) → OpenAI (vision analysis) → Notion (search prompt library) → Make Array Aggregator → OpenAI (choose style) → GPT Image 1.5 (edit image) → Google Drive (approval folder).

- Photos originate from a user-controlled Drive folder.
- Notion stores reusable style prompts and metadata.
- OpenAI analyzes composition and chooses a style before image editing.
- Outputs go to a manual review folder; no automatic social publishing.
- Daily scheduling and per-run limits are configured in Make.

## Public blueprint limitation

`blueprints/make-scenario.public-template.json` represents an **earlier five-module prototype**. It does **not** contain the live CloudConvert, vision, aggregation, or prompt-selection steps. All resource identifiers are placeholders. Do not import and activate without configuring and testing every module.

## Production considerations

- HEIC conversion, JPEG passthrough, file-size and format validation.
- Daily limit of one file per execution; avoid duplicates across manual runs.
- Error handlers, retries, cost monitoring, and filename uniqueness.
- Validate the model output mapping and final Drive upload.
- Review facial identity and image quality manually; AI editing cannot guarantee exact identity preservation.
