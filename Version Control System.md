# Version Control System (VCS)
## Links
Victors Git:
https://github.com/vpenso/scripts/blob/master/docs/code/git.md
### Allgemeines
- Versionsverwaltung von Dateien in einer durchsuchbaren Baumstruktur
- Verfügbarkeit über verschiedene Standorte hinweg und mit vielen anderen Personen gleichzeitig nutzbar
- Schutz vor Datenverlust
- Rückgängig machen von Änderungen
- Vergleich von Versione einer Datei
- Ein Repository ist eine Datenbank, in der Metadaten, Dateien und Versionen gespeichert werden
- Es gibt zentrale (Subversion) und dezentrale (Git) VCS
- Die VCS-Datenbank liegt in einer verteckten Datei im Repository
- Verschiedene Versionen des Repositorys werden von der VCS Software verwaltet

### Warum Git?
- Frei verfügbar und Open Source
- Sehr performant, da alles lokal läuft
- Integriertes Backup, wenn man das Repository auf verschiedene Maschinen synkronisiert
- Manipulationssicher, da jede Version mit SHA-1 (256bit) gehasht

### Infos:
- [Git](https://git-scm.com"git-scm Seite")
- [The Git Parable](http://tom.preston-werner.com/2009/05/19/the-git-parable.html"Git einfach erklärt")
- [Git Notes for Professionals book](https://goalkicker.com/GitBook/"Git kompliziert und ausführlich")

### Git Befehle:
- git init
- git status
- git add
- git commit -m ...
- git log
- git remote -u origin master <remoterepository anlegen>
