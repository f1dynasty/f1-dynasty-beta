# F1 Dynasty isolated beta preparation

Target: https://beta.f1dynasty.com only, in separate repository f1dynasty/f1-dynasty-beta. Production repository f1dynasty/f1-dynasty and its GitHub/Cloudflare workflows are never touched.

Keep this repository private and Pages disabled until owner approval. No public APK release or external TestFlight invitation is authorised. Commit only the two verified static ZIPs, package-checksums.json, this README and .github/workflows/beta-pages.yml. The local site/ tree is an audit mirror, not a second deployment input. No compilation/native cloud build is needed.

After approval, configure this separate repository Pages to GitHub Actions and custom domain beta.f1dynasty.com, detach ONLY the legacy beta Worker custom-domain binding and set beta CNAME to f1dynasty.github.io (DNS only). Leave production apex DNS, Cloudflare Pages and repository untouched. Verify DNS/HTTPS and manually dispatch with confirmation beta.f1dynasty.com and presentation 3d. No push trigger or automatic deploy exists. Configure an environment reviewer where the plan supports it.

Cloud and external analytics/auth are blocked by a beta-only META CSP. Local careers and intentional file backups remain available. The CSP permits the existing inline game/eval and same-origin iframe; it is a network-isolation boundary, not strict script-injection protection. Domain-scoped parent cookies may cross subdomains; the app ignores cookies and cloud auth is blocked.

Rollback: manually dispatch this same workflow with presentation classic to deploy the verified CURRENT repaired core without 3D at the SAME beta origin. Do not clear career storage, redirect users to production, or rebind to the older legacy beta Worker.
