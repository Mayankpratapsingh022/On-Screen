# On Screen

Public website and APK download page for On Screen, an Android assistant
experiment that can guide and perform native phone tasks through accessibility.

## Repository

GitHub repository name: `On-Screen`

GitHub repository description:

> Public website and APK download page for On Screen, an Android assistant experiment.

Expected GitHub Pages URL:

```text
https://mayankpratapsingh022.github.io/On-Screen/
```

## Contents

- `index.html` and `styles.css`: static GitHub Pages site.
- `assets/icons/`: copied app icons used by the page.
- `assets/icons/on-screen-icon-intro-transparent.webm`: optimized icon animation used by browsers.
- `assets/icons/on-screen-icon-intro-transparent.mov`: smaller transparent MOV fallback.
- `downloads/on-screen.apk`: checked-in APK fallback.
- `downloads/on-screen.apk.sha1`: checksum for the checked-in APK.

## Local preview

Open `index.html` directly in a browser. There is no build step.

## Publishing

GitHub repository names cannot contain spaces, so use `On-Screen` for the repo
slug while keeping the product name as `On Screen`.

Create a public repository, push this folder, then enable GitHub Pages from the
repository root on the `main` branch.

```bash
gh repo create Mayankpratapsingh022/On-Screen \
  --public \
  --description "Public website and APK download page for On Screen, an Android assistant experiment." \
  --source . \
  --remote origin \
  --push
```

Upload the APK as a release asset named `on-screen.apk` so the primary download
button points to the latest build:

```bash
gh release create v0.1.0 downloads/on-screen.apk \
  --repo Mayankpratapsingh022/On-Screen \
  --title "On Screen 0.1.0" \
  --notes "Initial APK build."
```

If you use a different repository name, update the release download URL in
`index.html` before publishing.
