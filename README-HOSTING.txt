SOHEL TAMRAKAR - WEBSITE HOSTING FILES

1. Extract this ZIP using your computer's Extract All / Uncompress option.
2. Upload index.html, app.js, styles.css and the complete assets folder to your host's public_html folder (or equivalent website root).
3. Keep index.html directly in the website root. Keep assets alongside it.
4. No build step, database, Node.js or ChatGPT account is required.

The assets folder contains the portrait, favicon and local fonts.
The house illustration is embedded SVG in index.html.
All website files match the existing published site version 3.

Current limitations preserved:
- Enquiry form uses EmailJS once serviceId, templateId and publicKey are configured in app.js. Without configuration or if sending fails, it offers an email draft fallback. It does not submit to the MortgageWorks CRM.
- index.html currently contains noindex,nofollow. Remove that robots tag when ready for search indexing.

Before independently launching, review dated scheme information and confirm company disclosures.

EMAILJS SETUP
- app.js is configured with the Outlook service and the Sohel website enquiry template. Keep only public identifiers in emailjsConfig; never add a private key or email password.
- Set the template recipient to soheltamrakar@mworks.com.au in EmailJS; do not use a visitor-controlled recipient.
- Template variables: {{name}}, {{email}}, {{phone}}, {{stage}}, {{suburb}}, {{message}}. Set Reply-To to {{reply_to}}.
- Use your connected email service as the sender, not the visitor’s address.
- Configure allowed domains and EmailJS spam protection as available in your account.
- Test from localhost or your HTTPS website, including success, failure and mobile behavior. Confirm inbox delivery before launch.
- Deploy the updated app.js, index.html and styles.css together. The EmailJS SDK loads from jsDelivr.
