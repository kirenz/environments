# Anaconda Umgebung erstellen :sparkles:

Diese Anleitung führt durch den Prozess, eine Datei von GitHub herunterzuladen und daraus eine Conda-Umgebung zu erstellen. 

Eine Conda-Umgebung ist wie ein Container, der eine spezifische Sammlung von Softwarepaketen und deren Abhängigkeiten enthält. Dies ermöglicht es, verschiedene Projekte mit unterschiedlichen Anforderungen zu verwalten, ohne dass es zu Konflikten zwischen den benötigten Paketen kommt. 

## Schritt 1: Anaconda Prompt oder Terminal öffnen

- **Windows**: Anaconda Prompt öffnen
- **macOS**: Terminal öffnen

## Schritt 2: Datei herunterladen

Folgenden Befehl eingeben, um die YAML-Datei herunterzuladen:

```bash
curl -O https://raw.githubusercontent.com/kirenz/environments/refs/heads/main/ws2425/env-genai.yml
```

Dieser Befehl lädt die Datei herunter und speichert sie im aktuellen Verzeichnis unter dem Namen `env-genai.yml`.

> [!NOTE]
> YAML ist eine Daten-Serialisierungssprache, die häufig zum Schreiben von Konfigurationsdateien verwendet wird. Die Dateien enthalten Textdaten, die in einer hierarchischen Struktur angeordnet sind und können als `.yaml` oder `.yml` verwendet werden.


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

Hinweise:

* **`conda`:**  Dies ist der Befehl zum Aufrufen der Conda-Paketverwaltung. Conda ist ein Werkzeug, das die Verwaltung von Paketen und Umgebungen für verschiedene Programmiersprachen, insbesondere Python, ermöglicht.
* **`env`:**  Dieser Unterbefehl von Conda bezieht sich auf die Verwaltung von Umgebungen. Mit `env` können verschiedene Umgebungen erstellt, aktiviert, deaktiviert oder entfernt werden.
* **`create`:**  Dieser Unterbefehl weist Conda an, eine neue Umgebung zu erstellen.
* **`-f env-genai.yml`:**  Diese Option gibt an, dass die neue Umgebung anhand einer YAML-Datei erstellt werden soll. 
    * `-f` steht für "file" (Datei).
    * `env-genai.yml` ist der Name der YAML-Datei, die die Spezifikationen für die Umgebung enthält, wie z. B. die Liste der zu installierenden Pakete und deren Versionen.
    * Diese YAML-Datei enthält eine Liste der Pakete und deren Versionen, die in der neuen Umgebung mit Hilfe von pip installiert werden sollen. Sie enthält auch die Python-Version und andere Einstellungen für die Umgebung festlegen. 



## Schritt 5: Neue Umgebung aktivieren

Nachdem die Umgebung erstellt wurde, diese mit folgendem Befehl aktivieren:

```bash
conda activate genai-om2
```



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
conda activate genai-om2
conda info --envs
```

Nach Abschluss dieser Schritte wurde erfolgreich eine Datei von GitHub heruntergeladen und daraus eine neue Conda-Umgebung erstellt.

Weitere Hinweise zu `.yml`-Dateien und Anaconda:

- [Erstellen einer Umgebung aus einer environment.yml-Datei](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file)

- [Manuelles Erstellen einer Umgebungsdatei](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-file-manually)



