# Sharing Akshar OCR AI on GitHub

## Recommended first release

1. Obtain company approval to publish the code, name and branding. Do not publish sample books, saved projects or confidential material.
2. Create a GitHub repository named `akshar-ocr-ai`. Choose Private for company-only sharing, or Public for an approved showcase.
3. Extract the source ZIP. Upload its contents using Git or GitHub Desktop. The included `.gitignore` excludes executables, model binaries, archives, private document formats and generated files. Add a code license only after the company decides which rights to grant.
4. Commit the source, README and third-party notices. Model/runtime binaries are distributed in the Windows release, not required in the source repository.
5. In the repository, open **Releases → Draft a new release**. Use a version tag such as `v1.0.0`, describe the tested features and limitations, and attach `Akshar-OCR-AI-Windows.zip` plus `SHA256SUMS.txt`.
6. Share the release link. Teammates download, extract and run the EXE. Private repositories require authorized GitHub access.

GitHub Releases instructions: https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository

## Can people use it directly through a GitHub link?

The download/release link is the correct simple way to distribute this Windows app. GitHub Pages can display screenshots, a guide and a download link, but it cannot run the Python/Tesseract backend. Uploading this app's HTML to Pages will not make a working hosted OCR service.

For a genuine browser-only shared service, a separate server deployment is needed: Python/Tesseract hosting, HTTPS, authentication, per-user storage, upload limits, job queues, resource limits and a company-approved data-retention policy. This local desktop build is not ready to be exposed publicly as a multi-user server.

GitHub Pages documentation: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

## Source development

Use Python 3.10+ on Windows and install `requirements.txt`. Run `python server.py`. The source archive includes Tesseract and initial language models; Git ignores them by default. On another source checkout, supply `ocr-engine/tesseract.exe` and models in `tessdata/`, or install Tesseract and let supported models download on demand. Windows teammates should use the packaged EXE instead.

To rebuild: install PyInstaller, then run `pyinstaller --noconfirm Akshar-OCR-AI.spec` from this folder. Output appears in `dist/`. Review third-party license obligations before redistributing.
