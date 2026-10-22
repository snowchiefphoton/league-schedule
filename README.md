# League Game Schedule Maker

One file (`index.html`), no installs. Open it in any browser to use it, or put it online for free so everyone in the league can open it.

## Free hosting option A: Netlify Drop (easiest, about 1 minute)
1. Put `index.html` in a folder by itself (for example `schedule-app`).
2. Go to https://app.netlify.com/drop and drag that folder onto the page.
3. Netlify gives you a link like `https://something.netlify.app`. Share it. (Create a free account so the site doesn't expire, and to rename the link.)

## Free hosting option B: GitHub Pages
1. Create a free account at https://github.com, then make a new **public** repository (for example `league-schedule`).
2. Click **Add file > Upload files**, upload `index.html`, and click **Commit changes**.
3. Open **Settings > Pages**, set Source to **Deploy from a branch**, choose branch `main` and folder `/ (root)`, then click **Save**. A minute later the site is at `https://YOUR-USERNAME.github.io/league-schedule/`.

## Using it
- Pick the season start and end dates and the number of teams, and rename teams if you want.
- Add any extra days off, one per line, like `2026-10-31`. US federal holidays are skipped automatically.
- **Allow teams to play more than once a week** (off by default): when off, each team plays only one day a week. When on, every Monday to Thursday play day gets a full game, and any team playing a 2nd (or later) time that week is marked with `*`, e.g. `Team 3*`. A legend explains the `*` under the calendar and list and at the bottom of the CSV. The Team summary shows each team's extra games.
- Click **Make schedule**. Then **Print** it, or **Download spreadsheet (CSV)**. The CSV opens in Excel or Google Sheets.

## Testing (optional, for developers)
`node test.js` checks the scheduling rules: Mon to Thu only, no holidays, no team twice in a week, and 2 or 3 teams per day. With the option on, it checks that every play day has a game, that the `*` marks are correct, and that the CSV has the legend.
