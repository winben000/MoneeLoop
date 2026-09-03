# MoneeLoop standalone website

This package contains the complete MoneeLoop prototype. It builds as a static website, so no server or database is required.

## Requirements

- Node.js 22.13 or newer
- npm 10 or newer

## Run locally

```bash
npm install
npm run dev
```

Open `http://localhost:3000`.

## Create the deployable website

```bash
npm install
npm run build
```

The finished static website will be generated in the `out` folder.

## Deploy with Vercel

1. Upload this folder to a GitHub repository.
2. In Vercel, choose **Add New → Project** and import the repository.
3. Vercel detects Next.js automatically. Keep the default build settings.
4. Select **Deploy**.

## Deploy with Netlify

1. Upload this folder to a GitHub repository.
2. In Netlify, choose **Add new site → Import an existing project**.
3. Use `npm run build` as the build command.
4. Use `out` as the publish directory.
5. Select **Deploy**.

## Deploy with Cloudflare Pages

1. Upload this folder to a GitHub repository.
2. Create a new Pages project and connect the repository.
3. Use `npm run build` as the build command.
4. Use `out` as the build output directory.
5. Select **Save and Deploy**.

## Deploy on another static host

Run `npm run build`, then upload everything inside the generated `out` folder to the public/root directory of your hosting provider.

## Routes

- `/` — landing page
- `/learn/` — learning dashboard
- `/lessons/emergency-fund-101/` — example LoopCourse lesson
- `/pricing/` — standalone pricing page

## Prototype behavior

- Lesson progress is stored temporarily in the browser session and resets after that browser tab/session is closed.
- The Premium plan selection buttons are demonstrations only; they are not connected to payment processing.
- The user profile and LoopToken balance are sample prototype data.

## Add your domain to social sharing metadata

The package intentionally omits an absolute social-preview image URL because your final domain is not known yet. After deployment, you can add `metadataBase: new URL('https://your-domain.com')` and the `/og.png` image to `app/layout.tsx` if you want link previews to use the included social card.
