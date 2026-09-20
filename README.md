# Hosni Eid — AI Portfolio

React + TypeScript + Tailwind + Lucide, built with Vite.

## Run
```
npm install
npm run dev        # local
npm run build      # outputs /dist (deploy to Vercel, Netlify or Cloudflare Pages)
```

## Where to edit
| What | File |
|---|---|
| Email, WhatsApp, social links, hero reel, main showreel | `src/data/site.ts` |
| Projects and case studies (add one = add an object) | `src/data/projects.ts` |
| All interface copy (services, workflow, about, tools...) | `src/content/en.ts` |
| Colors and fonts | `tailwind.config.js`, `src/index.css` |
| SEO, canonical URL, share image | `index.html` (replace `your-domain.com`, add `public/og.jpg`) |

## Adding media
Drop files into `public/media/`, then set paths in `projects.ts`:
```ts
thumbnail: '/media/skincare.jpg',
video: '/media/skincare.mp4',
gallery: [{ src: '/media/skincare-1.jpg' }, { src: '/media/skincare-2.mp4', poster: '/media/skincare-2.jpg' }],
```
Videos load lazily, only one plays at a time, and nothing plays under reduced-motion or data-saver.

## Adding Arabic later
1. Copy `src/content/en.ts` to `ar.ts` and translate the values.
2. Register it in `src/content/index.ts` and set `locale = 'ar'` (direction switches to RTL).
3. Per-project Arabic goes in each project's `translations: { ar: { ... } }`.
