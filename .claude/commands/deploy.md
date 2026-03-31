Deploy the current state of flowibs-apps to GitHub Pages.

Steps:
1. Run `cd ~/Projects/flowibs-apps && git status` to check for changes
2. If there are no changes, tell the user "No hay cambios pendientes para hacer deployment"
3. If there are changes, run `cd ~/Projects/flowibs-apps && git diff --stat` to show what changed
4. Stage all changes: `cd ~/Projects/flowibs-apps && git add .`
5. Create a commit with a descriptive message in Spanish summarizing the changes
6. Push to origin: `cd ~/Projects/flowibs-apps && git push origin main`
7. Tell the user: "Deployment completado. Los cambios estarán en https://apps.flowibs.com en ~1-2 minutos."
