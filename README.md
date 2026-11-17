# KRFA Demonlist

A Pointercrate-inspired, dark-themed Geometry Dash community demonlist starter.

## What's included
- Home page and statistics
- Main List and Extended List with search and sorting
- Individual level detail pages
- Player leaderboard
- Level submission form
- Local prototype admin tools
- JSON export/import backups
- Responsive desktop/mobile layout

## Run it on your computer
1. Download and extract the project.
2. Open `index.html` in a browser.
3. Use the navigation to explore the site.
4. Visit `#/admin` to try the local prototype admin tools.

The sample levels are placeholders. Replace them with real levels and verified information.

## Upload to GitHub
1. Create a GitHub repository named `krfa-demonlist`.
2. Set it to **Public** if you want to use the free GitHub Pages hosting option.
3. Upload `index.html`, `styles.css`, `app.js`, and this README to the repository root.
4. Open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select branch `main` and folder `/ (root)`, then save.
7. GitHub will provide the public website URL after deployment.

## Important: public website vs shared data
This starter is a static front-end. It stores changes in the current browser's `localStorage`. That means:
- Visitors can view the site.
- A submission is saved only in the browser where it was submitted.
- Admin edits are visible only in the browser where they were made.
- Data does not synchronize between your friends' devices.
- The `#/admin` page is a prototype, not a secure administrator login.

**Do not publish this as a fully functioning community submission system yet.** For shared submissions, persistent rankings, player accounts, moderator roles, and secure administration, connect a backend such as Supabase (database + authentication) or Firebase. Admin authorization must be enforced by backend security rules, never by a password or role stored in front-end JavaScript.

## Suggested next build phase
Connect Supabase:
- `levels` table: name, creator, verifier, level ID, rank, tier, difficulty, video, description
- `submissions` table: submitter, level details, video, status, created timestamp
- `players` and `records` tables
- Supabase Auth for moderator accounts
- Row Level Security policies: public read access to approved levels and records; authenticated users can submit; only moderator accounts can approve, edit, or delete

## Copyright / affiliation
KRFA is an independent fan project. Pointercrate is used as design inspiration only; this project does not include Pointercrate's code, branding, or assets. Geometry Dash is a trademark of its respective owner. This project is not affiliated with RobTop Games.
