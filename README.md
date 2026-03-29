![eberlabs_logo](B8D07AD5-2BE4-48A5-B180-414FE52EE634.PNG)

# 2Padel

[![CI](https://github.com/MariusxEb/proj_2padel/actions/workflows/ci.yml/badge.svg)](https://github.com/MariusxEb/proj_2padel/actions/workflows/ci.yml)
[![Live App](https://img.shields.io/badge/Web--App-2padel.eberlabs.de-ffd516?style=flat&logo=googlechrome&logoColor=white)](https://2padel.eberlabs.de)
[![Python 3.12](https://img.shields.io/badge/Python-3.12-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![Next.js 15](https://img.shields.io/badge/Next.js-15-000000?style=flat&logo=nextdotjs)](https://nextjs.org/)
[![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?style=flat&logo=docker&logoColor=white)](https://docs.docker.com/compose/)
[![Playwright](https://img.shields.io/badge/Automation-Playwright-45ba4b?style=flat&logo=playwright&logoColor=white)](https://playwright.dev/)

**2Padel** bucht Padel-Courts auf Bookaball automatisch — vollautomatisch um Mitternacht, ohne dass du dabei sein musst.

---

## Das Problem: Warum 2Padel?

Auf Bookaball werden neue Court-Slots täglich um Mitternacht freigegeben. Beliebte Zeiten sind innerhalb von Minuten ausgebucht — wer nicht sofort zur Stelle ist, schaut in die Röhre.

Manuell um Mitternacht buchen zu wollen bedeutet: Wecker stellen, schläfrig ins Handy tippen, hoffen, dass man schnell genug ist. Das ist unzuverlässig und auf Dauer nervig.

**2Padel übernimmt das für dich.** Einmal konfiguriert, bucht die App deinen Court ab sofort automatisch — pünktlich, zuverlässig, jeden Tag.

---

## Was 2Padel für dich tut

Wenn du einmal festgelegt hast, an welchen Wochentagen du spielen möchtest und zu welcher Uhrzeit, erledigt 2Padel den Rest:

1. Täglich prüft die App, ob in den nächsten Wochen ein Buchungsdatum ansteht
2. Sobald Mitternacht naht, öffnet 2Padel Bookaball in einem automatisierten Browser
3. Die App meldet sich mit deinen Zugangsdaten an und bucht den Court
4. Das Ergebnis — Erfolg oder Misserfolg mit Details — siehst du danach in deiner Buchungshistorie

Du musst dabei nicht wach sein. Du musst nichts tun. Die App läuft rund um die Uhr auf einem dedizierten Server.

---

## Funktionen

### 🎾 Automatische Court-Buchung um Mitternacht
Die App öffnet Bookaball eigenständig und schließt die Buchung innerhalb eines von dir festgelegten Zeitfensters ab (Standard: 00:01–08:59 Uhr). So wird kein Slot verpasst, auch wenn du schläfst.

### ⚙️ Persönliche Buchungskonfigurationen
Du legst selbst fest, an welchen Wochentagen du spielen möchtest, zu welcher Uhrzeit und wie weit im Voraus gebucht werden soll (zwischen 1 und 6 Wochen). Mehrere Konfigurationen sind möglich — z. B. für verschiedene Tage oder Zeiten.

### 🏖️ Abwesenheitsverwaltung
Du fährst in Urlaub oder machst eine Pause? Trage einfach den Zeitraum als Abwesenheit ein. Die App überspringt alle Buchungsdaten innerhalb dieses Zeitraums automatisch — keine versehentlichen Buchungen während deiner Auszeit.

### 📋 Buchungshistorie
Unter „Meine Buchungen" siehst du alle vergangenen Buchungsversuche: wann gebucht wurde, ob es geklappt hat, welcher Court reserviert wurde und welchen Betrag du bezahlt hast. Bei Fehlern gibt es Schritt-für-Schritt-Protokolle, die zeigen, was schiefgelaufen ist.

### 🔒 Sichere Datenspeicherung
Deine Bookaball-Zugangsdaten und Kreditkartendaten werden verschlüsselt gespeichert. Sie sind im System zu keinem Zeitpunkt im Klartext abrufbar — auch nicht für Administratoren.

### 👤 Benutzerverwaltung
Neue Konten werden nach der Registrierung von einem Administrator freigeschaltet. Admins können Konten aktivieren, deaktivieren und verwalten.

---

## Die Bereiche der App

| Bereich | Was du dort tust |
|---------|-----------------|
| **Dashboard** | Schnellübersicht: Wie viele Konfigurationen sind aktiv? Wann war die letzte erfolgreiche Buchung? Gibt es fehlende Einstellungen? |
| **Automationen** | Buchungskonfigurationen erstellen, bearbeiten, aktivieren, deaktivieren und löschen |
| **Meine Buchungen** | Alle Buchungsversuche einsehen — mit Status, gebuchtem Court, Betrag und Detailprotokoll |
| **Einstellungen** | Bookaball-Zugangsdaten hinterlegen, Kreditkartendaten speichern, Abwesenheiten verwalten, Account löschen |
| **Admin** | *(nur für Administratoren)* Nutzerkonten aktivieren, deaktivieren und löschen |

---

## Erste Schritte

Neu bei 2Padel? So richtest du dich ein:

**1. Registrieren**
Erstelle ein Konto über die Registrierungsseite. Dein Account wird anschließend von einem Administrator aktiviert — danach kannst du dich einloggen.

**2. Bookaball-Zugangsdaten hinterlegen**
Gehe zu **Einstellungen** und trage deinen Bookaball-Benutzernamen und dein Passwort ein. Diese Daten benötigt die App, um sich in deinem Namen auf Bookaball anzumelden.

**3. Kreditkartendaten hinterlegen**
Ebenfalls unter **Einstellungen**: Hinterlege die Kreditkarte, mit der die Court-Buchungen bezahlt werden sollen. Alle Daten werden verschlüsselt gespeichert.

**4. Buchungskonfiguration erstellen**
Gehe zu **Automationen** und erstelle deine erste Konfiguration. Wähle aus:
- An welchen Wochentagen du spielen möchtest
- Zu welcher Uhrzeit (z. B. 18:00 Uhr)
- Wie weit im Voraus gebucht werden soll (z. B. 3 Wochen)

**5. Fertig — die Automation läuft**
Ab sofort prüft 2Padel täglich, ob ein Buchungsdatum ansteht, und bucht deinen Court automatisch. Das Ergebnis siehst du unter **Meine Buchungen**.

---

## Wie funktioniert die App im Hintergrund?

Für alle, die es genauer wissen wollen — ohne technisches Vorwissen:

2Padel läuft auf einem Server, der rund um die Uhr online ist. Die App besteht aus mehreren Komponenten, die zusammenarbeiten:

```
Deine Konfiguration
       ↓
  Scheduler prüft alle 5 Minuten: Steht heute eine Buchung an?
       ↓
  Um Mitternacht: Browser-Automation öffnet Bookaball
       ↓
  Anmeldung mit deinen Zugangsdaten → Court auswählen → Bezahlen → Bestätigen
       ↓
  Ergebnis wird gespeichert und ist in "Meine Buchungen" sichtbar
```

- **Der Scheduler** ist ein Hintergrundprozess, der ständig läuft und prüft, ob eine Buchung ansteht.
- **Die Browser-Automation** (Playwright) steuert einen echten Webbrowser — genau so, als würdest du selbst auf Bookaball klicken.
- **Die Datenbank** speichert alle Konfigurationen, Ergebnisse und verschlüsselten Zugangsdaten.
- **Die Web-App** ist deine Oberfläche, über die du alles einrichten und einsehen kannst.

Es wird immer nur eine Buchung pro Konfiguration pro Tag erstellt — auch wenn die App neu startet oder mehrfach prüft. Doppelbuchungen sind technisch ausgeschlossen.

---

## Unterstützte Plattformen

| Plattform | Status |
|-----------|--------|
| Bookaball | ✅ Vollständig unterstützt |
| neue Plattformen | 🔜 In Planung |
