# Daily Spend

A daily expense tracker with a pet panda you feed by logging every day, plus a monthly calendar, a budget, levels and CSV export.

It is a single static page: everything lives in `index.html`, with no build step and no dependencies.

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

## Data

Entries are stored in the browser's `localStorage`, so they stay on the device and browser you log them in. Use **Monthly export** to save a month as a CSV file.

## Deploy

Import the GitHub repository in Vercel and deploy with the default settings (framework preset "Other", no build command).
