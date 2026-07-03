# RLV Bedarfsrechner

Bedarfsrechner für die Risikolebensversicherung (Hinterbliebenenabsicherung) im ERGO Corporate Design.

**Live:** https://phoeser.github.io/rlv-bedarfsrechner/

## Was der Rechner macht

Ermittelt aus Alter, Familie und Einkommen die monatliche Versorgungslücke der Hinterbliebenen
im Todesfall sowie das zur Schließung erforderliche Kapital:

1. **Nettoeinkommen** – Näherung nach Steuerklasse III (Einkommensteuertarif 2025, SV-Sätze 2025, Kirchensteuer je Bundesland, Kinderfreibeträge)
2. **Gesetzliche Hinterbliebenenrente** – kleine (25 %) / große (55 %, altes Recht 60 %) Witwen-/Witwerrente plus Waisenrente (10 % je Kind unter 26), kalibriert am Dialog-Bedarfsrechner
3. **Versorgungslücke** = Netto (oder Versorgungswunsch) − Hinterbliebenenrenten − vorhandene Absicherung
4. **Erforderliches Kapital** = Lücke × Rentenbarwertfaktor (monatlich vorschüssig, gewählter Zinssatz und Dauer)

## Technik

- Eine einzige HTML-Datei (`index.html`), kein Build, keine Abhängigkeiten
- Berechnung komplett clientseitig (JavaScript), Diagramm als Inline-SVG
- Deployment über die zentrale Datei `auto_deploy.html` (GitHub Contents API + Pages)

## Hinweis

Der Rechner ist ein Hilfsmittel und ersetzt keine qualifizierte Beratung.
Alle Ergebnisse sind Näherungswerte ohne Gewähr.
