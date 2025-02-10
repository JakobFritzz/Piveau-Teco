# Piveau-Teco Repository

## Überblick / Overview

Dieses Repository enthält die Hauptkomponenten sowie Submodule für die Piveau-Teco-Instanz. Um das Repository korrekt zu klonen und die Submodule zu initialisieren, folgen Sie bitte den untenstehenden Anweisungen.

This repository contains the main components and submodules for the Piveau-Teco instance. Please follow the instructions below to correctly clone and initialize the repository and its submodules.

---

## 📜 Anleitung (Deutsch)

### 1. Repository klonen
Clonen Sie das Haupt-Repository wie gewohnt:
```bash
git clone https://github.com/JakobFritzz/Piveau-Teco.git
```

### 2. Submodule initialisieren
Nach dem Klonen müssen die Submodule initialisiert und aktualisiert werden:
```bash
cd Piveau-Teco
git submodule update --init --recursive
```

Dieser Befehl:
- Initialisiert die Submodule.
- Klont die Submodule aus den entsprechenden Repositories.
- Synchronisiert die Submodule mit den im Haupt-Repository referenzierten Commits.

### 3. Änderungen in Submodulen
Submodule sind eigenständige Git-Repositories. Änderungen in einem Submodul müssen dort separat committed und gepusht werden.

#### Beispiel:
1. Gehen Sie in das Submodul-Verzeichnis:
   ```bash
   cd ky_docker-compose/piveau-docker-compose
   ```
2. Nehmen Sie Änderungen vor und committen Sie:
   ```bash
   git add .
   git commit -m "Submodule changes"
   git push
   ```
3. Aktualisieren Sie die Submodul-Referenz im Haupt-Repository:
   ```bash
   cd ../../
   git add ky_docker-compose/piveau-docker-compose
   git commit -m "Updated submodule reference"
   git push
   ```

### 4. Submodule auf dem neuesten Stand halten
Um sicherzustellen, dass die Submodule aktuell sind, führen Sie diesen Befehl regelmäßig aus:
```bash
git submodule update --remote
```

---

## 📜 Instructions (English)

### 1. Clone the repository
Clone the main repository as usual:
```bash
git clone https://github.com/JakobFritzz/Piveau-Teco.git
```

### 2. Initialize submodules
After cloning, initialize and update the submodules:
```bash
cd Piveau-Teco
git submodule update --init --recursive
```

This command:
- Initializes the submodules.
- Clones the submodules from their respective repositories.
- Synchronizes the submodules with the commits referenced in the main repository.

### 3. Making changes in submodules
Submodules are independent Git repositories. Changes in a submodule must be committed and pushed separately.

#### Example:
1. Navigate to the submodule directory:
   ```bash
   cd ky_docker-compose/piveau-docker-compose
   ```
2. Make changes and commit them:
   ```bash
   git add .
   git commit -m "Submodule changes"
   git push
   ```
3. Update the submodule reference in the main repository:
   ```bash
   cd ../../
   git add ky_docker-compose/piveau-docker-compose
   git commit -m "Updated submodule reference"
   git push
   ```

### 4. Keeping submodules up to date
To ensure the submodules are up to date, run this command regularly:
```bash
git submodule update --remote
```

---

## Wichtige Hinweise / Important Notes

- Submodule-URLs sind in der Datei `.gitmodules` gespeichert und werden automatisch aktualisiert, wenn Submodule hinzugefügt oder geändert werden.
- Jeder Nutzer muss die Submodule nach dem Klonen initialisieren, um Zugriff auf die vollständige Projektstruktur zu haben.

- Submodule URLs are stored in the `.gitmodules` file and are automatically updated when submodules are added or changed.
- Each user must initialize the submodules after cloning to access the complete project structure.
