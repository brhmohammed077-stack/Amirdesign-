# Amirdesign

Bilingual Arabic/French landing page for professional PowerPoint and Word design requests.

## Included
- Responsive design with Arabic RTL and French LTR layout
- Service cards, process explanation, and order form
- Form validation, deadline, file/reference link, and consent
- Safe configuration placeholder for a form backend
- No secrets or API keys in browser code

## Important: email is not active by default
A static website cannot securely send email by itself. The form intentionally shows a setup message until a form backend endpoint is configured.

### Recommended simple setup: Formspree
1. Create an account at https://formspree.io/ and create a form.
2. Set the notification/recipient email to `goldennarthur@gmail.com` in Formspree. Complete any verification they require.
3. Copy the form endpoint URL they provide (usually `https://formspree.io/f/FORM_ID`).
4. Open `config.js` and set:
   `formEndpoint: "https://formspree.io/f/YOUR_FORM_ID"`
   Replace the example with your actual endpoint. Never put API keys or passwords here.
5. Test with a sample request and check the inbox and spam folder.

The included JavaScript sends JSON. If your chosen form provider only accepts standard HTML form submissions, use that provider's documented AJAX/JSON endpoint or adapt the fetch request to its documented format. Confirm this with a real test before advertising the site.

## Deploy on GitHub Pages
1. Create a new public GitHub repository named `amirdesign`.
2. Upload `index.html`, `styles.css`, `script.js`, `config.js`, and `README.md` to the repository root.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**, choose `main` and `/(root)`, then Save.
5. Wait for the published URL shown in Settings → Pages.
6. After configuring the form endpoint, test on both mobile and desktop.

## Alternative: Netlify
1. Sign in to https://www.netlify.com/ and choose **Add new site → Deploy manually**.
2. Upload the site files (or drag the unzipped folder into the deployment area).
3. Configure `config.js` with the real form endpoint and redeploy.
4. Add a custom domain later if desired.

## Before launch
- Verify the notification address in your form provider.
- Test Arabic and French language switching.
- Send a test request and verify the email arrives.
- Check the spam folder.
- Add a privacy policy if you begin collecting more personal information or uploaded files.
- Do not promise delivery dates or prices until confirmed directly with each customer.
