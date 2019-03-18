# Notizen Linux

### Fragen


### Editoren
- Atom - Text Editor - nur Grafisch
- Neovim - neuer VI (VIM) - läuft überall

### ToDos:
- gmail anlegen
- Für Todolisten todotxt.org anschauen

### Bash Befehle:
- echo $SHELL
- sudo dpkg -i atom-amd64.deb (Atom installieren)
- sudo apt --fix-broken install (fehlende Pakete nachziehen)
history (Liste der letzen Befehle anzeigen)
- export Editor=vim
- echo $editor
- mkdir <name> Verzeichnis erstellen

### Tmux Terminal Multiplexer
- https://leanpub.com/the-tao-of-tmux
- Config Datei in Git legen und lokal einen Link im Homeverzeichnis erstellen, damit Tmux die Config beim öffnen lädt
- config Datei:
# keybinding to split Windows
bind r source-file ~/.tmux.conf \; display-message "Reload ~/.tmux.conf"
bind h split-window -h
bind v split-window -v

# keybinding to pane switch with Alt arrows
bind -n M-Left select-pane -L
bind -n M-Right select-pane -R
bind -n M-Up select-pane -U
bind -n M-Down select-pane -D

# keybinding to make resizing easier
bind -n Left resize-pane -L
bind -n Right resize-pane -R
bind -n Up resize-pane -U
bind -n Down resize-pane -D



### Zeichenkodierung
- ASCII
- Unicode

### Markdown
- Dillinger zum konvertieren von markdown in andere Formate
