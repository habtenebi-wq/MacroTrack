# MacroTrack

A mobile-friendly nutrition and fitness tracker with calorie and macro tracking, weight progress, and a level-up system with user-made daily quests. Everything runs in the browser and is saved in local storage, so there is no account or backend.

## Features

- **Calorie calculator:** BMR (Mifflin-St Jeor), maintenance calories (TDEE) and a suggested daily target for losing, maintaining or gaining weight. Metric or imperial units.
- **Custom goals:** editable calorie, protein, carb and fat targets, with macro calories checked against your calorie goal (4/4/9 kcal per gram).
- **Food log:** breakfast, lunch, dinner and snacks. Search built-in foods or add your own, edit, duplicate or delete entries, plus recent foods, saved meals and a custom food list.
- **Dashboard:** progress rings, calories remaining, date navigation and supportive messages when you go over a goal.
- **Progress:** weight log with a line chart, start/current/goal stats, and weekly insights.
- **Quests and levels:** create your own daily quests (water, steps, push-ups, anything). Clearing quests and unlocking achievements earns XP and raises your level and rank.
- **Accessibility and design:** dark mode, sidebar on desktop and bottom navigation on mobile, labeled inputs, keyboard navigation and screen-reader-friendly charts.

## Run it

It is a single static file. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

An internet connection is needed because React, Babel and Tailwind load from CDNs.

## Deploy with GitHub Pages

1. Push this folder to a GitHub repository.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, and save.
4. Your site will be live at `https://<your-username>.github.io/<repo-name>/`.

## Tech notes

- React 18 and TypeScript, written inline in `index.html` (inside the `<script type="text/plain" id="src">` block) and compiled in the browser with Babel.
- Tailwind CSS via the Play CDN, which is meant for prototyping. For production, move to a build setup such as Vite with Tailwind installed locally.
- Data lives in `localStorage` under the key `macrotrack-v1`. Use **Profile → Reset sample data** to restore the demo data.

## Disclaimer

MacroTrack gives estimates only. It is not medical advice, and no results are guaranteed. Talk with a doctor or registered dietitian before making major changes to your diet. Built-in food nutrition values are approximate.

## License

MIT. See `LICENSE`.
