# Homepage Review

Date: 2026-03-30

## Findings

1. High: The page is not publishable yet because the contact and social actions are placeholders. The CTA points to contact, but the only contact detail is `deine-email@beispiel.de`, and both social links are `#`, so users hit dead ends instead of usable next steps. See `index.html:106`, `index.html:147`, `index.html:148`, `index.html:158`.

2. High: For a German club homepage, `Impressum` and likely `Datenschutz` are missing. That is a real launch risk, not a cosmetic issue. This is not legal advice, but for a public-facing site in Germany this needs checking before the page goes live.

3. Medium: The gallery pulls images from GitHub raw URLs instead of using local relative paths. That adds an unnecessary external dependency to render your own assets, makes local and offline preview less faithful, and is brittle if the branch or repo path changes. These should just be local files. See `index.html:138`, `index.html:139`, `index.html:140`.

4. Medium: The page currently reads as a generic template rather than a real club homepage. The copy is mostly placeholder-level, there is no concrete venue, date, contact, or organizer information, and no visual identity from the provided sticker or logo is used at all. That means the current draft does not yet communicate trust or authenticity.

5. Low: The converted PNGs look visually fine and preserve transparency, but they are much heavier than the original sticker WebP for no visible gain: about `74 KB` for the WebP versus about `407 KB` for each PNG. If this becomes the site logo, using the PNGs as-is is wasteful unless PNG is specifically required.

6. Low: There is some asset clutter and duplication in the repo root. `IMG-20260330-WA0000(1).jpg` and `WhatsApp Image 2026-03-30 at 15.29.57.jpeg` appear to be the same image content, and the `temp` folder holds conversion intermediates rather than production assets. That will get messy quickly once more drafts arrive.

## Open Questions and Assumptions

- This review assumes the draft is intended to become a real public club homepage rather than only a visual mockup.
- This review also assumes the WhatsApp sticker is intended to become the site logo.

## Summary

The PNG conversion itself looks acceptable. The Windows and Linux outputs appear effectively identical in visible quality and transparency handling.

The bigger issues are on the homepage side: it is still a template draft, lacks key launch information, and does not yet use the available branding asset in a coherent way.

## Files Reviewed

- `index.html`
- `bilder/galerie/vereinsfoto.jpg`
- `bilder/galerie/gartenszene.jpg`
- `bilder/galerie/marktszene.jpg`
- `bilder/logo/logo-vorschau.jpg`
- `WhatsApp Image 2026-03-30 at 15.29.57.jpeg`
- `temp/WhatsApp Sticker 2026-03-30 at 15.16.49.webp`
- `temp/output.png`
- `temp/output.linux.png`
