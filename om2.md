# Anleitung

Diese Anleitung führt durch den Prozess, eine Datei von GitHub herunterzuladen und daraus eine Conda-Umgebung zu erstellen. Die Anleitung funktioniert sowohl für Windows (mit Anaconda Prompt) als auch für macOS (mit Terminal).

## Schritt 1: Anaconda Prompt oder Terminal öffnen

- **Windows**: Anaconda Prompt öffnen
- **macOS**: Terminal öffnen

## Schritt 2: Datei herunterladen

Folgenden Befehl eingeben, um die YAML-Datei herunterzuladen:

```bash
curl -O https://raw.githubusercontent.com/kirenz/environments/refs/heads/main/ws2425/env-genai.yml
```

Dieser Befehl lädt die Datei herunter und speichert sie im aktuellen Verzeichnis unter dem Namen `env-genai.yml`.

## Schritt 3: Überprüfen, ob die Datei heruntergeladen wurde

Je nach Betriebssystem den entsprechenden Befehl eingeben, um den Inhalt des aktuellen Verzeichnisses anzuzeigen:

- **Windows (Anaconda Prompt)**:
  ```
  dir
  ```

- **macOS (Terminal)**:
  ```
  ls
  ```

`env-genai.yml` sollte in der Liste der Dateien erscheinen.

## Schritt 4: Conda-Umgebung erstellen

Den folgenden Befehl verwenden, um eine neue Conda-Umgebung aus der heruntergeladenen YAML-Datei zu erstellen:

```bash
conda env create -f env-genai.yml
```

Dieser Prozess kann einige Minuten dauern, da alle erforderlichen Pakete heruntergeladen und installiert werden.

## Schritt 5: Neue Umgebung aktivieren

Nachdem die Umgebung erstellt wurde, diese mit folgendem Befehl aktivieren:

```bash
conda activate genai
```

Hinweis: Der Name der Umgebung kann in der YAML-Datei anders definiert sein. Den Befehl gegebenenfalls anpassen.

## Schritt 6: Überprüfen der aktiven Umgebung

Um zu überprüfen, ob die neue Umgebung erfolgreich aktiviert wurde, eingeben:

```bash
conda info --envs
```

Dies listet alle verfügbaren Umgebungen auf. Die aktive Umgebung wird mit einem Sternchen (*) gekennzeichnet.

## Zusammenfassung

Hier sind noch einmal alle Befehle in der richtigen Reihenfolge:

```bash
curl -O https://raw.githubusercontent.com/kirenz/environments/refs/heads/main/ws2425/env-genai.yml
# Für Windows: dir
# Für macOS: ls
conda env create -f env-genai.yml
conda activate genai
conda info --envs
```

Nach Abschluss dieser Schritte wurde erfolgreich eine Datei von GitHub heruntergeladen und daraus eine neue Conda-Umgebung erstellt.