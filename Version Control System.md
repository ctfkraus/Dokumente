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

### Bis jetzt umgesetzt
ToDo! (code makieren nachschauen und umsetzen)
- github Repository mit [git clone] lokal gespeichert
   - dazu git installiert incl. Xcode
   - den Pfad kann man bei github kopieren
   - für lesen braucht man kein github PW, aber sudo ist nötig
- lokal Dateien in den Working Tree kopiert und mit [git add + git commit] zum lokalen Repository hinzugefügt
   - [git commit] will Kommentar
   - in ubuntu ging dabei Nano auf
   - gegoogelt, wie nano grob funktioniert
   - ToDo! Umstellen auf nvim - lokalen Pfad in Ubuntu und OSX umstellen - WIE?
- mit [git push] das Repository auf github aktualisiert
   - dafür ist der Account von github nötig, um dort schreiben zu können
- mit [git pull] ein geklontes Repository unter OSX und eins unter Ubuntu aktualisiert
   - [git pull] braucht auch sudo rechte
