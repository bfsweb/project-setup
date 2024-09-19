# CD Bund Project Setup

## Einleitung

Diese Anleitung erklärt Schritt für Schritt, wie du das offizielle Website-Template des Bundes verwenden und auf Plesk hochladen kannst.

## Anforderungen
- Node
- NPM

### Schritt 1: Projekt clonen
Wir möchten den aktuellen Code herunterladen und ihn lokal auf unserem Comutper bearbeiten können.

- Öffne das commandline tool deiner Wahl auf deinem Laptop (z.B. Terminal)
- Navigiere zum Ordner in welchen du das Projekt lokal ablegen willst
- Clone das designsystem reposiory mit dem folgenden command:
```zsh
git clone https://github.com/swiss/designsystem.git
```
- Du solltest jetzt einen neuen Ordner namens "designsystem" haben. Navigiere in diesen hinein:
```zsh
cd designsystem
```
- Installiere alle notwendigen Pakete mit diesem command:
```zsh
npm install
```
- Starte das Projekt lokal mir diesem command:
```zsh
npm run dev:nuxt
```
- Du solltest das Projekt jetzt lokal in einem Browser deiner wahl unter [localhost:3000](http://localhost:3000/) sehen können. Falls dem nicht so ist, könnte es sein dass du Probleme mit node, npm oder nvm hast. Am besten kopierst du die error-message in deiner commandline auf chatGPT. Bei derartigen Versionsproblemen ist ein wenig AI Hilfe sehr zielführend.

### Schritt 2: Repository auf GitHub einrichten
Wir möchten die Änderungen an deinem neuen Projekt zurückverfolgen können. Dafür richten wir ein Repository auf GitHub ein.

- Gehe zur GitHub Seite unseres Teams: [bfsweb](https://github.com/bfsweb?tab=repositories)
- Klicke auf den "Neu" Knopf oben rechts um ein neues Repository zu eröffnen.
- Gib dem Repository einen deskriptiven Namen und eine kurze Beschreibung.
- Setze die Sichtbarkeit des Projekts auf "privat".
- Aktiviere die Option "Repository mit einem README erstellen".
- Klicke unten auf "erstellen".
- Kehre zu deinem commandline tool zurück. Stelle sicher, dass du in der root des designsystem Ordners bist:
```zsh
pwd
```
- In deiner commandline, stelle sicher, dass du in der root des "designsystem" Ordners bist. Initialisiere den Ordner als git-ordner:
```zsh
git init
```
- Verlinke deinen lokalen Ordner mit dem remote Repository mit dem folgenden command (Du musst die url des neuen repositories einfügen):
```zsh
git remote add origin https://github.com/bfsweb/<name-deines-repositories>
```
- Füge die files, welche du lokal hast zum remote repository hinzu mit diesen commands:
```zsh
git add .
```
```zsh
git commit -m "feat: initial commit"
```
```zsh
git push -f origin head
```

Gratuliere, du hast ein Repository für deinen Quellcode erstellt und es mit deinem lokalen Code verlinkt 🥳

### Schritt 3: GitHub in Plesk integrieren
Um Code nicht von Hand auf Plesk laden zu müssen, wird in diesem Schritt die Plesk-GitHub Integration vorgenommen. Änderungen im Repository werden so direkt auf dem Server vorgenommen.

- Melde dich in Plesk an und gehe zur Übersicht deiner Domain.
