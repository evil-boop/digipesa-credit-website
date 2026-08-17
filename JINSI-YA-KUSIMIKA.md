# DigiPesa Credit Ltd — Jinsi ya Kusimika Tovuti na Kuwa Admin

## Muundo wa faili
```
index.html          → Ukurasa mkuu wa tovuti
data/content.json    → Maudhui yanayobadilika (bidhaa, mawasiliano, FAQ)
admin/index.html      → Dashibodi ya admin (Decap CMS)
admin/config.yml      → Mipangilio ya nini kinachoweza kuedit-iwa
netlify.toml           → Mipangilio ya Netlify
```

## Hatua 1 — Pandisha kwenye GitHub
1. Tengeneza akaunti/ repo mpya GitHub (mfano `digipesa-credit-website`).
2. Pakia (upload) faili zote hizi kwenye repo hiyo, ukitunza muundo wa folda kama ulivyo.

## Hatua 2 — Unganisha na Netlify
1. Nenda [netlify.com](https://netlify.com) → fungua akaunti bure kwa email ya kampuni.
2. "Add new site" → "Import an existing project" → chagua GitHub → chagua repo yako.
3. Publish directory: `.` (tayari imewekwa kwenye netlify.toml) → Deploy.
4. Baada ya dakika chache utapata link kama `digipesa-credit.netlify.app` (unaweza kubadilisha jina kwenye Site settings, au kuunganisha domain yako halisi ya DCL baadaye).

## Hatua 3 — Washa Netlify Identity (kwa ajili ya admin login)
1. Kwenye dashboard ya site: **Site configuration → Identity → Enable Identity**.
2. Chini ya **Registration**, chagua "Invite only" (ili si kila mtu ajisajili mwenyewe).
3. Nenda **Identity → Services → Git Gateway → Enable Git Gateway** (hii inaruhusu admin panel kuhifadhi mabadiliko moja kwa moja kwenye GitHub repo yako).

## Hatua 4 — Jialike mwenyewe kama Admin
1. Kwenye tab ya **Identity**, bofya **Invite users** → weka email yako (na za wenzako wa IT/Management wanaotakiwa ku-edit).
2. Utapokea email — bofya link, weka password.
3. Fungua `https://[jina-la-site-lako].netlify.app/admin/` → login na email/password uliyoweka.

## Hatua 5 — Washa Notifications za Contact Form
1. Kwenye dashboard: **Forms** tab → utaona fomu ya "contact" ikionekana baada ya deploy ya kwanza.
2. **Settings → Form notifications → Add notification → Email notification** → weka email ya timu ya mauzo/mikopo itakayopokea ujumbe kila mtu anapotuma fomu.

## Jinsi ya kutumia Admin Dashboard baadaye
- Fungua `/admin/`, login.
- Utaona "Ukurasa wa Nyumbani" wenye sehemu: Hero, Bidhaa (NISOGEZE/SME), Mawasiliano, FAQ.
- Badilisha chochote (riba, namba za simu, maswali) → bofya **Publish**.
- Netlify ita-deploy tovuti upya kiotomatiki ndani ya sekunde chache — hakuna haja ya kugusa code.

## Muhimu
- Kabla ya kuchapisha rasmi, hakikisha umebadilisha taarifa zote zenye alama ya `*` kwenye `data/content.json` (kupitia admin panel) na anwani/simu/email halisi za DCL.
- Ongeza taarifa za leseni/regulator (BOT au inayohusika) kwenye footer ya `index.html` kabla ya go-live rasmi.
