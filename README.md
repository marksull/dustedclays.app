# dustedclays.app

Single-page site for the DustedClays iOS + watchOS app, served by GitHub Pages
at **https://dustedclays.app**.

Everything is static — `index.html` with inline CSS and the images in
`assets/`. No build step.

## Enabling GitHub Pages (one-time)

1. GitHub → repo **Settings → Pages**.
2. Source: **Deploy from a branch** → branch `main`, folder `/ (root)` → Save.
3. Under **Custom domain**, `dustedclays.app` should appear automatically (from
   the `CNAME` file). Tick **Enforce HTTPS** once the certificate is issued
   (can take a few minutes after DNS is in place).

## DNS records (at your domain registrar)

For the apex domain `dustedclays.app`, add four **A** records:

```
dustedclays.app.  A  185.199.108.153
dustedclays.app.  A  185.199.109.153
dustedclays.app.  A  185.199.110.153
dustedclays.app.  A  185.199.111.153
```

Optional but recommended, for `www.dustedclays.app`:

```
www  CNAME  marksull.github.io.
```

Until DNS propagates, the site is reachable at
https://marksull.github.io/dustedclays.app/.

## App Store note

The Privacy section anchor — **https://dustedclays.app/#privacy** — is written
to serve as the app's privacy-policy URL in App Store Connect.

## Updating screenshots

Screenshots come from the simulators via the DEBUG-only demo mode in the app
repo (`~/Development/apple/clay`). Launch with `SIMCTL_CHILD_DEMO_SEED=1`,
`SIMCTL_CHILD_DEMO_TAB=…` or `SIMCTL_CHILD_DEMO_SCREEN=…` and capture with
`xcrun simctl io <device> screenshot`.
