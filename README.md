# BARBERO Salon — Hostinger Node.js upload

This archive contains the prebuilt production website and a small Node.js static-file server. It does not need a database, API keys, or an environment file.

## Upload to Hostinger

1. In hPanel, open **Websites → Add Website → Node.js web app** and choose **Upload your files**.
2. Upload `BARBERO-Hostinger-Node.zip`.
3. Use **Node.js 22** (Hostinger's current default/LTS) and **npm**.
4. Set the framework to **Other** if Hostinger asks for one.
5. Set the entry file to `server.js`. Leave the build command and output directory empty; the website is already built in `public/`.
6. Deploy. Hostinger installs the package and starts the app with `npm start`.

The archive root contains `package.json`, `package-lock.json`, `server.js`, and `public/`, so it can be extracted directly as the application root. Do not upload this ZIP as a static site to `public_html`; use the Node.js Web App upload flow.

## Local check

With Node.js 18–24 installed, run:

```sh
npm start
```

The server reads Hostinger's `PORT` environment variable and falls back to port 3000 for local use.

## Before going live

- `BARBERO` is the temporary salon name in the website configuration.
- The appointment form opens WhatsApp with a prefilled enquiry; the customer still has to send the message, and the salon must confirm the appointment.
- Confirm that the supplied phone number is active on WhatsApp before accepting enquiries.
- The review total is labeled as owner-provided. Check the Google Maps search link and update the count if needed.
- Social links are blank until real URLs are added in the website configuration.

Hostinger's upload flow and build settings: https://docs.hostinger.com/node.js/creating-an-app
