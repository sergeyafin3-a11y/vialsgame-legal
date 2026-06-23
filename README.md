# Legal pages — Vials: ASMR Sand Sort Puzzle

Static Privacy Policy + Terms of Service for the app stores. Hosted free on
**GitHub Pages** at the `vialsgame.com` custom domain.

Final URLs (what you paste into App Store Connect / Google Play):

- Privacy Policy: `https://vialsgame.com/privacy.html`
- Terms of Service: `https://vialsgame.com/terms.html`

## Developer details (filled in)

Both documents name:

- **Individual Entrepreneur Afinogenov Sergei Olegovich**, registered in the
  Republic of Armenia, registration / taxpayer No. `2408000572`.
- Governing law: Republic of Armenia.
- Contact: `vialsgame.play@gmail.com`.

The effective/updated date is set to 23 June 2026 — bump it if you ship later.

### Assumes the release ships analytics + ads + cloud

`privacy.html` already describes Firebase analytics/Crashlytics, AdMob rewarded
ads (+ AppLovin/Meta/Mintegral mediation), and iCloud / Play Games cloud save —
because these are planned for release (currently `Stub*` in code, tracked in
`docs/TECH_DEBT.md`). **If any of these is cut before launch, delete its row in
the section-2 table and its bullet in section 4** so the policy does not
over-declare.

> The **App Privacy "Nutrition Label" (ASC)** and **Data Safety (Google Play)**
> forms are a separate thing from this policy: they must match the *submitted
> binary*. Fill/update them in the same release that turns on the real SDKs —
> not before. While the services are stubs, the first build declares only
> "Purchases".

## Hosting — GitHub Pages with custom domain (free, HTTPS)

1. Create a **new public repo** (e.g. `vialsgame-legal`).
2. Copy the contents of this `legal/` folder into the repo root
   (`index.html`, `privacy.html`, `terms.html`, `CNAME`).
3. Repo → **Settings → Pages** → Source: `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. In the **Custom domain** field enter `vialsgame.com` (the `CNAME` file already
   contains it). Tick **Enforce HTTPS** once the cert is issued (a few minutes).
5. At your domain registrar, point DNS to GitHub Pages:
   - Apex `vialsgame.com` → four `A` records:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - (optional) `www` → `CNAME` to `<your-username>.github.io`
6. Wait for DNS to propagate, then open `https://vialsgame.com/privacy.html`.

> If you'd rather not use the apex domain yet, you can skip the CNAME/DNS steps
> and use the default `https://<username>.github.io/vialsgame-legal/privacy.html`
> URL — Apple and Google accept any public HTTPS URL.
