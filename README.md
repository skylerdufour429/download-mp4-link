# 森のカーニバル — MP4 download page

A static, GitHub Pages-ready video landing page with a GitHub Codespaces devcontainer.

## Configure the video

Edit `app-config.js` and set `videoUrl` to a direct MP4 URL you own or are authorized to distribute:

```js
window.APP_CONFIG = {
  videoUrl: "./media/authorized-video.mp4"
};
```

For a local file, create `media/` and add your authorized MP4 there. For large videos, use a file host/CDN that permits direct downloads; GitHub Pages is intended for static sites, not large video hosting. Some external hosts block cross-origin requests or ignore browser download hints. In that case, the "Open video source" link remains available and the host controls downloading.

## Run in Codespaces

1. Create a GitHub repository and upload these files.
2. Open the repository, choose **Code → Codespaces → Create codespace on main**.
3. In the terminal run `npm start`.
4. Open the forwarded port 8000.

## Deploy to GitHub Pages

1. Push the files to the `main` branch.
2. In repository **Settings → Pages**, set the build/deployment source to **GitHub Actions**.
3. The workflow in `.github/workflows/pages.yml` deploys the static site after pushes to `main`.
4. Open **Settings → Pages** to find the published site URL.

GitHub Pages sites are publicly accessible. Do not publish private files, and only distribute media for which you have the necessary rights.
