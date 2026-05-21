# love-cycle-redirect

Single static page (`redirect.html` at repo root) that forwards HTTPS redirects to the mobile app deep link.

Enable **GitHub Pages** from the `main` branch (root `/`) or copy `redirect.html` to any static host.

## Usage

| App | Redirect page URL |
|-----|-------------------|
| Production | `https://your-host/redirect.html` |
| Staging | `https://your-host/redirect.html?env=staging` |

Opens `lovecycle://auth/callback` or `lovecycle-staging://auth/callback` and forwards query/hash (`?code=`, `?session_id=`, `#access_token=`, …).

**Staging Supabase Site URL** (if you use this page for auth):  
`https://your-host/redirect.html?env=staging`

**Stripe `APP_URL` on staging** must include the query flag, e.g. set the secret to  
`https://your-host/redirect.html?env=staging`  
so checkout success URLs become `…/redirect.html?env=staging&session_id=…`.
