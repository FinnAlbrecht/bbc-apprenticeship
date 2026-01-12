# BBC Apprenticeship Projects

---
## Example badges and README structure which I use in my sub-projects
![GitHub last commit](https://img.shields.io/github/last-commit/FinnAlbrecht/bbc-apprenticeship)
![GitHub repo size](https://img.shields.io/github/repo-size/FinnAlbrecht/bbc-apprenticeship)
![GitHub top language](https://img.shields.io/github/languages/top/FinnAlbrecht/bbc-apprenticeship)
![GitHub language count](https://img.shields.io/github/languages/count/FinnAlbrecht/bbc-apprenticeship)
![GitHub branch check runs](https://img.shields.io/github/check-runs/FinnAlbrecht/bbc-apprenticeship/main)
![GitHub contributors](https://img.shields.io/github/contributors/FinnAlbrecht/bbc-apprenticeship)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/FinnAlbrecht/bbc-apprenticeship)
![GitHub repo stars](https://img.shields.io/github/stars/FinnAlbrecht/bbc-apprenticeship?style=social)
![GitHub forks](https://img.shields.io/github/forks/FinnAlbrecht/bbc-apprenticeship?style=social)

---

This repository contains various projects, exercises, and code snippets developed during my vocational training at **BBC (Berufsbildungscenter)**, 2023–2024.

During this time, I gained experience in a wide range of topics, including:

- Operating Systems (Windows / Linux)
- Python
- JavaScript
- Java / JavaFX
- Spring Boot
- React / React Native
- SQL
- Git / GitHub
- Docker / Cloud basics

---

## 📁 Contents

| Project | Date | Description |
|--------|------|-------------|
| [Vacation Assignment](https://github.com/FinnAlbrecht/vacationAssignment/blob/main/README.md) | Oct 2024 | Small web app project for managing vacation requests. Built with Next.js and Node.js. |
| [Python Basics](./01_python_grundlagen/README.md) | Feb 2024 | Simple Python scripts and exercises covering loops, functions, and file handling. |
| [Web Development](./02_webentwicklung/README.md) | Mar 2024 | HTML, CSS, and JS fundamentals. Responsive layouts and forms. |
| [SQL & Databases](./03_sql_datenbanken/README.md) | Apr 2024 | Example SQL queries and schema design exercises. |
| [Java Practice](./04_java_übung/README.md) | May 2024 | Object-oriented programming exercises in Java. |

---

## 🧠 Goals

The purpose of this repository is to document my learning journey and showcase my progress throughout the apprenticeship.  
Each project folder contains its own README with more detailed information about tools, versions, and concepts used.

---

## ℹ️ Notes on Version Control

Please note that the projects in this repository were **pushed to GitHub retrospectively**.  
The original development and commit history were maintained on a **private internal BBC Git instance** during the apprenticeship.

This public repository serves as a curated overview and portfolio of the work completed during that time.

## Submodule Setup: Schritt-für-Schritt-Anleitung

### Erstmalige Initialisierung von Submodules

1. **Submodules initialisieren und herunterladen**
```bash
   git submodule init
   git submodule update
```
   
   Oder als Kurzform:
```bash
   git submodule update --init --recursive
```

2. **Branch-Tracking für ein Submodule konfigurieren**
   
   Damit dein Submodule automatisch einem bestimmten Branch folgt (z.B. `main`):
```bash
   git config -f .gitmodules submodule.placeholder.branch main
   git add .gitmodules
   git commit -m "Configure submodule to track main branch"
   git push
```

### Submodule auf den neuesten Stand bringen

Wenn du die neuesten Änderungen aus dem Submodule-Repository holen möchtest:
```bash
# 1. Submodule auf neuesten Stand des konfigurierten Branches aktualisieren
git submodule update --remote placeholder

# 2. Änderungen im Hauptrepository registrieren
git add placeholder

# 3. Commit mit aussagekräftiger Nachricht erstellen
git commit -m "Update submodule placeholder to latest main"

# 4. Änderungen pushen
git push
```

### Repository mit Submodules klonen

Wenn jemand das Repository neu klont:
```bash
# Option 1: Alles in einem Schritt
git clone --recurse-submodules <repository-url>

# Option 2: Nach normalem Clone
git clone <repository-url>
cd <repository-name>
git submodule update --init --recursive
```

### Häufige Befehle

- **Status aller Submodules prüfen**: `git submodule status`
- **Alle Submodules aktualisieren**: `git submodule update --remote --recursive`
- **In ein Submodule wechseln**: `cd vacationAssignment` (dort kannst du normal mit Git arbeiten)
