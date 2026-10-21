# CNHS Student Data Bank Website

A simple static website for **Calinan National High School** with the school logo on the left side of the header and a Microsoft Forms collection area. It is designed for GitHub Pages.

## Important limitation

GitHub Pages hosts static files only. This website does **not** create a secure student database or save submissions itself. Microsoft Forms collects the responses, and authorized school staff manage the responses in Microsoft Forms/Excel. Never put actual student records or response spreadsheets in this public GitHub repository.

## 1. Connect Microsoft Forms

1. Sign in to the school's Microsoft 365 account and create a Microsoft Form for the approved student data collection purpose.
2. Add only the fields the school needs. Provide the school's approved privacy notice and any required parent/guardian authorization.
3. In Microsoft Forms, open **Collect responses** / **Share** and copy the link respondents use.
4. Find the **Embed** option (`</>`) and copy the iframe/embed URL.
5. Open `index.html` and replace:
   - `PASTE_MICROSOFT_FORMS_EMBED_URL_HERE` with the embed URL.
   - `PASTE_MICROSOFT_FORMS_PUBLIC_URL_HERE` with the respondent link.
6. Save the file and test the form locally in your browser.

## 2. Publish using GitHub Pages

1. Sign in to GitHub and create a new repository, for example `CNHS-Student-Data-Bank`.
2. Upload `index.html`, `README.md`, and the entire `assets` folder (including `cnhs-logo.png`) to the repository root.
3. Open the repository's **Settings → Pages**.
4. Under build/deployment, select **Deploy from a branch**.
5. Choose branch `main` and folder `/(root)`, then click **Save**.
6. Wait for GitHub Pages to publish. Open the URL shown on the Pages settings screen.

## 3. Recommended Microsoft Forms settings

- Use the school's managed Microsoft account, not a personal account.
- Set who can respond according to school policy (for example, organization-only when all respondents have school accounts, or anyone-with-link only if approved and appropriate).
- Limit who can view and export responses to authorized staff.
- Do not request passwords or collect unnecessary sensitive information.
- Do not store student data, response exports, or private spreadsheets in this public repository.
- Because students may be minors, follow school/DepEd privacy processes and obtain required authorization/consent before collection.

## Files

- `index.html` — website page
- `assets/cnhs-logo.png` — supplied school logo

The provided response URL (https://forms.cloud.microsoft/r/WySRTtFMaG) is connected to the form button and used as the initial iframe source. If the form does not embed correctly, copy the dedicated iframe URL from Microsoft Forms' Embed option and replace the iframe src in index.html.
