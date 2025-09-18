Bijdragen aan OOSDD GroceryApp

🌳 Branches

main

Bevat stabiele productiecode.

Elke release krijgt hier een tag (bv. v1.0.0).

develop

Basis voor alle nieuwe features.

Hier komt code samen die in de volgende release gaat.

feature/*

Begin altijd vanaf develop.

Naamgeving: feature/korte-omschrijving (bv. feature/login-form).

Na afronden: maak een Pull Request naar develop.

release/*

Begin vanaf develop wanneer een nieuwe release wordt voorbereid.

Hier fix je laatste bugs en documentatie.

Merge naar main én terug naar develop.

hotfix/*

Begin vanaf main bij urgente productieproblemen.

Na fix: merge naar main én naar develop.

🔄 Workflow
1. Nieuwe feature starten
git checkout develop
git checkout -b feature/naam-van-feature

2. Feature afronden

Commit en push je wijzigingen.

Maak een Pull Request naar develop.

Laat je code reviewen door een teamgenoot.

3. Release voorbereiden
git checkout develop
git checkout -b release/1.0.0


Test en los laatste bugs op.

Merge naar main en develop.

Voeg een tag toe:

git tag -a v1.0.0 -m "Release v1.0.0"
git push origin v1.0.0

4. Hotfix uitvoeren
git checkout main
git checkout -b hotfix/1.0.1


Fix de bug.

Merge naar main en develop.

Tag de release:

git tag -a v1.0.1 -m "Hotfix v1.0.1"
git push origin v1.0.1
