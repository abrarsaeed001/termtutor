# TermTutor web app

The TermTutor web app is built with [Next.js](https://nextjs.org/) and React. It currently uses the default Next.js starter page and is not yet connected to the Python prototype.

## Requirements

- Node.js and npm

## Local development

From this directory, install the locked dependencies and start the development server:

```bash
npm ci
npm run dev
```

Open [http://localhost:3000](http://localhost:3000). Changes to files in `app/` are reflected during development.

## Quality checks

```bash
npm run lint
npm run build
```

Run both commands from this directory before submitting web app changes.

## Application structure

- `app/page.tsx` — home page.
- `app/layout.tsx` — shared layout, fonts, and page metadata.
- `app/globals.css` — global styles.
- `public/` — static assets served by Next.js.

See the [Next.js documentation](https://nextjs.org/docs) for framework guidance.
