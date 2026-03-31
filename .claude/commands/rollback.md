Rollback the last deployment on flowibs-apps.

Steps:
1. Run `cd ~/Projects/flowibs-apps && git log --oneline -10` to show recent versions
2. Show the user the list and ask which version they want to revert to
3. If they say "la anterior" or "la última", revert the most recent commit: `cd ~/Projects/flowibs-apps && git revert HEAD --no-edit`
4. If they specify a commit hash, revert that specific commit: `cd ~/Projects/flowibs-apps && git revert <hash> --no-edit`
5. Push the revert: `cd ~/Projects/flowibs-apps && git push origin main`
6. Tell the user: "Rollback completado. La versión anterior estará activa en https://apps.flowibs.com en ~1-2 minutos."
