# Partner Application — Google Form Setup

I can't create Google Forms directly (no Forms API access), but this takes about 5 minutes to build yourself. Go to **forms.google.com** → **Blank form**, title it "Partner Application — The Language Blueprint LLC", and add these fields in order:

1. **Full Name** — Short answer, required
2. **Email** — Short answer, required (Settings → Response validation → Email)
3. **Phone** — Short answer
4. **Area(s) of Expertise** — Checkboxes, allow "Other":
   - District & School Consulting
   - Private Student Instruction (SLIFE / Multilingual Learners)
   - Academic & Professional Writing Coaching
   - Teacher Mentorship / Coaching
   - AI-Enhanced Learning Tools
5. **Certifications / Credentials** — Paragraph (e.g. NYS certification area, TESOL/Applied Linguistics degree, relevant licenses)
6. **Years of Experience** — Short answer or Dropdown (0–2, 3–5, 6–10, 10+)
7. **Current Caseload Capacity** — Short answer ("How many clients/projects could you take on right now?")
8. **Geographic Area / Districts You Can Serve** — Short answer
9. **Why do you want to partner with The Language Blueprint LLC?** — Paragraph, required
10. **Resume / CV** — File upload (Google Forms supports this natively; requires responders to be signed into a Google account to upload)
11. **LinkedIn or Portfolio URL** — Short answer, optional
12. **How did you hear about us?** — Short answer or Dropdown

**Settings to turn on** (gear icon):
- Collect email addresses: On
- Response receipts: "Always"
- Restrict to 1 response: your choice (off is usually fine for recruiting)

Once built, click **Send** → copy the **link** (use the "Shorten URL" checkbox for a clean `forms.gle/...` link) and send it to me — I'll wire it into the "Apply to Partner" button on `partner.html`, replacing the `REPLACE_WITH_PARTNER_FORM_LINK` placeholder.

Responses land automatically in a connected Google Sheet if you click the Sheets icon in the Responses tab — recommended so you have a running list of applicants.
