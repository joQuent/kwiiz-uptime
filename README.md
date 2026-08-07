# kwiiz-uptime

Moniteur d'uptime **externe** de [kwiiz.ch](https://kwiiz.ch) : un cron GitHub Actions
sonde les 3 domaines (`kwiiz.ch`, `teacher.kwiiz.ch`, `go.kwiiz.ch`) toutes les
6 minutes depuis l'infrastructure GitHub, donc indépendamment du serveur surveillé.
En cas de panne : alerte Telegram (au plus 1/heure), puis un message de retour à la
normale. L'état courant est dans le fichier [`state`](state).

Complète le check interne du serveur (qui voit nginx tomber mais pas un serveur
entièrement mort). Détail : `docs/roadmap/capacite-serveur.md` du dépôt principal.
