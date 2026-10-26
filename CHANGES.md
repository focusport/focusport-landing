# What changed in this version

- Home hero: new centered hero with your cavern photo (slow drift and light pulse, CSS only, stops with "reduce motion").
- Fonts: Bricolage Grotesque (headings) and Hanken Grotesk (text), self-hosted. Inter, JetBrains Mono and Instrument Serif removed.
- Removed generated-looking details: all-caps labels, arrows on buttons, dotted proof lines, the old tilted-phone hero, the promo screenshots.
- New page windows.html: free app and website blocker for Windows (Allowlist and Blocklist modes, Task Manager/restart/shutdown protection, Bulletproof mode, schedules, Android vs Windows table, FAQ with structured data). The "Windows" nav item now opens it; the Microsoft Store button is on the page.
- Fixed the empty screenshot frames: a global rule hid lazy images until a script marked them loaded.
- Removed the hero byline; the "replies within 24 hours" promise is in every footer, the contact page and the FAQ.
- Hedged unverified competitor claims in the comparison tables ("Free Forever", "Opal / Freedom", prices).
- MOBILE AND TABLET: the header now collapses to a menu button below 1100px (the old styles targeted a wrapper that did not exist, so the desktop links overflowed on phones). The menu panel now opens (it waited for a class that no script added). Section margins are consistent on phones, the hero sits flush under the header, and nothing widens the page at 360, 390, 768, 1024 or 1440px. Tested in headless Chromium.
- Hero stats bar: 4.7 rating, 6.2L+ focus hours completed, cross-device sync (Android + Windows), in a glass bar like your reference.
- FIXED A SITE-WIDE BUG: the main script on all 14 inner pages had a syntax error (a leftover fragment), so the FAQ accordion, theme toggle and mobile menu did nothing. Repaired and syntax-checked.
- FAQ answers no longer peek out when closed (padding moved to the open state).
- Windows app screens are now drawn in HTML/CSS (sharp at any size, follow the light/dark theme) instead of low-resolution images: start screen, schedule screen and a new focus screen. The home page shows a tilted Windows window. The focus screen is a new design, so match it to your real app before relying on it.
- Windows app screens added (home cross-device section, features page, professionals page). Broken "Windows" nav links on all inner pages now go to the Microsoft Store.
- Inner pages: the old promo images are replaced by real app screens built in HTML/CSS. Duplicate galleries removed.
- Theme: dark by default (saved choice wins), toggle restored on the home header, theme set before first paint.
- SEO: new titles and descriptions, robots, Open Graph and Twitter tags, richer structured data, sitemap dates.
- Speed: unused images removed, hero served as WebP (66 KB desktop, 28 KB mobile), CSS minified (readable source in src/styles.src.css).
- Fixed three broken blocks in the old stylesheet (two lost media queries and an orphaned animation).

## To do before publishing
- Replace assets/hero/hero-1920.webp with a 2560x1440 version of the cavern image (the source was only 1024x576 and looks soft on large screens).
- Verify the 6.2L+ focus hours figure and where it comes from, and the rating (4.7), the number of ratings (220+) and the installs on the day you publish.
- Confirm the Windows rows (Task Manager, restart and shutdown, Bulletproof mode) and the supported Windows versions (10 and 11) before publishing windows.html.
- Confirm whether Android also has a Blocklist mode (see the TODO in windows.html).
- Test every row of the "What you can't do during a session" table on real phones, including safe mode.
- Edit styles in src/styles.src.css, then re-minify into styles.css.

## Update 26 Oct 2026
- Ratings changed from 130+ to 220+ (visible text and ratingCount in structured data on index.html). Verify against Google Play/Microsoft Store on publish day.
- windows.html: new "Why the Windows lock is hard to get around" section, "FocusPort vs typical PC blockers" table, 3 new FAQs.
- faq.html: new group 5 (strict Windows blocking, sync, alternatives), 6 questions, also in FAQ structured data.
- 3 new posts: strict-app-blocker-for-windows, freedom-alternative-windows-android, sync-focus-sessions-windows-android. Added to blog index, sitemap, llms.txt.
- No existing URL was renamed or removed.
- KEEP the old sccreen-1..5.webp files on the server (the live site and its Open Graph tags still point to them).

## Update 2 (26 Oct 2026)
- New apps.html (Our Apps): FocusPort Android, FocusPort for Windows, Brainrot Limit (launching soon), more coming soon. Linked from home page section and every footer; in sitemap and llms.txt.
- contact.html: the in-page email form is removed. Topics are now mailto links with the subject prefilled.
- Footer: the boxed Microsoft Store button on blog pages is now a normal link ("Windows App (Microsoft Store)").

## Update 3 (26 Oct 2026)
- Brainrot: Reel Limit is now live in apps.html (Google Play + brainrot.focusport.in), with its logo (brainrot-logo.webp). FocusPort Android and Windows cards use the FocusPort icon; the Windows one has a Windows badge.
- Blockit: Schedule and Allowlist changed to Yes in the Android comparison table, and the Blockit text rewritten to match. Check Blockit's Play page once before publishing.
- Privacy: the "Zero Web Trackers" claim is replaced with "Basic App Analytics" (Firebase Analytics for onboarding and first-session completion). New "Product Analytics" section in privacy-policy.html, plus fixes in features.html, llms.txt and llms-full.txt.
- TODO: make the Play Data safety form, the privacy policy at focusport.github.io/focusport-privacy, and brainrot.focusport.in/privacy.html say the same thing.

- Restored the Google (google-site-verification) and Bing (msvalidate.01) verification tags on index.html, copied from the live site. Do not remove them.
