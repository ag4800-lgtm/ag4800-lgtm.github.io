# Partner Application Form

The partner application now lives directly on the site at `partner-application.html`, using the same pattern as the client intake form (a plain HTML form submitting via Formspree — no backend, no separate Google Form).

## Setup

1. Go to **formspree.io** and create a **new form** (name it something like "Partner Applications" — keep it separate from the contact and intake forms so submissions are easy to filter).
2. Copy the form ID Formspree gives you.
3. Replace `YOUR_PARTNER_FORM_ID` in `partner-application.html`'s `<form action="https://formspree.io/f/YOUR_PARTNER_FORM_ID">` with that ID.

That's it — Formspree doesn't require you to predefine fields in their dashboard; it just receives whatever the HTML form sends and emails it to you.

## Fields included on the page

- Full Name, Email, Phone
- Area(s) of Expertise (checkboxes: District & School Consulting, Private Student Instruction, Academic & Professional Writing Coaching, Teacher Mentorship/Coaching, AI-Enhanced Learning Tools)
- Certifications / Credentials
- Years of Experience (dropdown)
- Current Caseload Capacity
- Geographic Area / Districts You Can Serve
- Why do you want to partner with us? (required)
- Resume / CV (file upload — Formspree supports this natively)
- LinkedIn or Portfolio URL
- How did you hear about us?
