# Portiond marketing website

Static HTML/CSS marketing site for https://www.portiond.com/, deployed through the existing Vercel project connected to this repository. This is separate from the Portiond event application. No framework, package manager, server, database or component-library migration is needed.

## Preview

```sh
python3 -m http.server 4175 --bind 127.0.0.1
```

Open http://127.0.0.1:4175/. Vercel continues serving the repository root as the static site. There is no application build step, TypeScript or package-based lint command.

## Early access

The page embeds the **existing** Tally form `GxqLDQ`, with direct links to https://tally.so/r/GxqLDQ if the widget is unavailable. Existing hash-based Tally popup links still work through the retained embed script. The old `#waitlist` anchor is retained. All primary CTAs point to `#early-access`.

Tally owns validation, persistence and confirmation. The marketing page does not intercept submissions, save emails in browser storage, or display its own success message. No subscribers were migrated, deleted, exported or created by this change. No analytics SDK or submission tracking was added.

### Remaining provider-side work before acquisition launch

These changes require access to edit **the same form**, not a replacement:

- Make email the only required field. Current Tally validation also requires beta interest and a newsletter-preference answer.
- Add optional event type (workshops, retreats, community events, recreational activities, training, other) and hosting frequency.
- Retain separate newsletter consent and update the form introduction to the broader event-operations positioning.
- Verify the intended privacy policy/controller: the existing form currently links to `revflow.co.uk/legal/privacy-policy`. Do not substitute an invented policy.
- Configure and verify duplicate handling in Tally, including previously subscribed addresses. Preserve subscriber records and avoid revealing subscriber details.
- Submit an owner-approved test email, confirm the submission in Tally, test repeat submission, and verify provider success/error behavior. Empty-form validation and rendering alone do not prove persistence.

## Product previews and claim boundaries

`assets/*.jpg` are genuine captures of the existing application's local prototype on November 2, 2026: `/events`, `/register/1`, `/payments` and the workshop overview. The demo notices remain visible. All visible records are existing prototype sample data, not customer metrics. No records were created for the screenshots. Full captures are 1440×1000; 720px variants reduce mobile downloads. Images open at full size through ordinary links.

Event drafts and manual payment review are implemented in the application, with live configuration/pilot validation still required. Public registration, provider checkout, secure document storage, e-signatures and connected reporting are not represented as launched. Do not replace these qualifiers with availability claims until the application's actual release supports them.

## Verification

- Checked at desktop 1440×1000 and mobile 390×844; mobile document width matches the viewport without horizontal overflow.
- All screenshot assets load. Explicit dimensions reserve layout space; gallery images are lazy loaded and responsive.
- Primary signup and secondary workflow anchors reach their intended sections below the sticky header.
- Existing Tally embed loads and rejects an empty submission with required-field errors. No real submission or duplicate/persistence test was performed because provider administration and an approved test address are unavailable.
- Native FAQ disclosures work with Enter. Skip link, focus-visible styles, semantic landmarks and heading hierarchy are included.
- HTML anchor, local image/srcset and metadata integrity checks, CSS parse and `git diff --check` run against the static source. No project lint/typecheck/build scripts exist; none were invented solely for this page.
- SEO title, description, canonical, Open Graph, image alt text and social card metadata are included. No invented reviews, prices, release dates or structured-data claims.

Deploy via the existing Vercel Git workflow after review. Do not deploy this repository through the event application's Sites project. Production publication and provider-side form changes are separate from the local page implementation.
