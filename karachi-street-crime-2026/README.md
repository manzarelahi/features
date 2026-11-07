# Karachi street crime 2026 — interactive feature

Self-contained Urdu (RTL) page: `index.html`. No build step; it only loads Google Fonts. It has no headline or byline, so add your own above the embed.

## Embed on your site

Host `index.html` anywhere (or use GitHub Pages), then paste:

```html
<iframe id="khi-crime-2026" src="https://YOUR-HOST/karachi-street-crime-2026/index.html"
        style="width:100%;border:0;min-height:900px" loading="lazy"
        title="کراچی اسٹریٹ کرائم 2026"></iframe>
<script>
  window.addEventListener('message', function (e) {
    if (e.data && e.data.type === 'khi-crime-2026-height') {
      document.getElementById('khi-crime-2026').style.height = e.data.height + 'px';
    }
  });
</script>
```

The script resizes the iframe to fit the content, so readers never see a second scrollbar.

## Data (1 Jan – 5 Nov)

| | 2025 | 2026 |
|---|---|---|
| Street crime incidents | 54,850 | 46,617 |
| Killed | 68 | 65 (police: 51 while resisting) |
| Injured | 272 | 182 |
| Mobile phones snatched | 14,587 | 16,821 |
| Cars snatched/stolen | 1,843 | 1,301 |
| Motorcycles snatched/stolen | 38,420 | 28,495 |

2026 vehicles + bikes: 4,273 snatched, 25,523 stolen. Daily rates are over 309 days.

## Fonts

Urdu text uses **Nafees Web Naskh**, loaded from
[manzarelahi/myfonts](https://github.com/manzarelahi/myfonts) (`nafeesweb.woff`, then `nafeesweb.ttf`) via jsDelivr:

    https://cdn.jsdelivr.net/gh/manzarelahi/myfonts@main/nafeesweb.woff

Backup font: Noto Naskh Arabic (Google Fonts). Numbers use Inter.

Note: the current `nafeesweb` files contain only Latin letters, digits and punctuation,
so Urdu text falls back to Noto Naskh Arabic until they are replaced with a complete
Nafees Web Naskh. After replacing them, jsDelivr may serve the old file for up to 7 days;
to refresh it right away, open
`https://purge.jsdelivr.net/gh/manzarelahi/myfonts@main/nafeesweb.woff` (and the `.ttf` one).
