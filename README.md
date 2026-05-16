# Nightlife guide sites (static)

Two static HTML sites in one repo for Cloudflare Pages:

| Folder | Site |
|--------|------|
| `jungpm-nightlife-guide/` | JungPM / BLINDUP |
| `angelie-night/` | Angelie Night |

## Cloudflare Pages (per site)

1. **Workers & Pages** → Create → Connect to Git → select this repo.
2. **Framework preset:** None  
3. **Build command:** *(leave empty)*  
4. **Build output directory:**  
   - JungPM: `jungpm-nightlife-guide`  
   - Angelie: `angelie-night`  
5. Create **two** Pages projects if you host both domains.

If the repo list is empty, on GitHub go to **Settings → Applications → Cloudflare Pages** and grant access to this repository (or “All repositories”).
