# Case Number Extractor

A free, browser-based tool that extracts Case / CMS numbers from PDF, Word, Excel, and photo files. Built for Sajjad Ahmad (Punjab LMS / PST case monitoring).

## How to deploy this on GitHub Pages (free hosting)

1. Create a new **public** repository on GitHub (e.g. `case-number-extractor`).
2. Upload everything in this zip to the repo, keeping the folder structure exactly as-is:
   - `index.html` (the tool itself)
   - `.github/workflows/deploy.yml` (the auto-deploy workflow)
   - `README.md`
3. Go to your repo's **Settings → Pages**.
4. Under "Build and deployment", set **Source** to **"GitHub Actions"**.
5. Push (or just uploading the files via the GitHub web UI and committing) will automatically trigger the workflow.
6. After a minute or two, check the **Actions** tab — once the "Deploy to GitHub Pages" run shows a green checkmark, your site will be live at:

   ```
   https://<your-username>.github.io/<repo-name>/
   ```

That URL is now a permanent, shareable link to the tool — no more downloading/re-downloading files, no caching confusion. Just open that link on any phone or computer.

## Updating the tool later

Any time you (or Claude) edit `index.html` and push the change (or re-upload it via the GitHub web UI), the workflow re-runs automatically and the live site updates within a minute or two.

## Notes

- The tool uses a free OCR.space API key for scanned photos/PDFs. Paste your own free key in the box at the top of the page (get one instantly at ocr.space/ocrapi) for better reliability than the shared demo key.
- No backend/server needed — everything runs in the visitor's browser plus the OCR.space cloud API call for scanned content.
