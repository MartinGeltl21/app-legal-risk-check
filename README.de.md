# App Legal Risk Check

Ein wiederverwendbarer Agent-Skill für sechs rechtliche Risikobereiche von Web-Apps und die Prüfung passender technischer Korrekturen.

[English / vollständige Installationsanleitung](README.md) · [Skill](SKILL.md) · [Primärquellen](references/legal-sources.md) · [MIT-Lizenz](LICENSE)

## Was wird geprüft?

1. **Signup / COPPA:** Zielgruppe, Alters- und Elternfreigaben, frühe Datenerhebung.
2. **Externe Fonts:** Browser-Datenübermittlung, lokales Hosting, verbleibende Anfragen.
3. **Session Replay / CIPA:** Aktivierung, Einwilligung, Widerruf und Maskierung.
4. **Marketing / CAN-SPAM:** Absender, Postanschrift, funktionierende Abmeldung und Versandsperre.
5. **Abos:** Verlängerungsbedingungen, Zustimmung, Bestätigung und Kündigung.
6. **Nutzer-Uploads / DMCA:** einschlägige Agentenregistrierung, Kontaktdaten und Meldeprozesse.

Jeder Aufruf behandelt alle sechs Bereiche. Nicht anwendbare Punkte werden begründet. Ergebnisse enthalten Status, Belege und konkrete Restaufgaben.

## Installation und Aufruf

In Codex eingeben:

```text
Nutze $skill-installer, um den Skill aus
https://github.com/MartinGeltl21/app-legal-risk-check zu installieren.
Die SKILL.md liegt im Repository-Stammverzeichnis.
```

Alternativ stehen in der [englischen README](README.md#install-in-codex) Git-Befehle für Windows, macOS und Linux. Der Skill ist auf Englisch geschrieben, antwortet aber in deiner Sprache.

Nur prüfen:

```text
Nutze $app-legal-risk-check und prüfe alle sechs Bereiche meiner App.
Ändere keine Dateien. Nenne Belege und offene Aufgaben.
```

Prüfen und umsetzen:

```text
Nutze $app-legal-risk-check vor dem Launch. Behebe anwendbare technische
Lücken, prüfe die betroffenen Abläufe und nenne notwendige externe Schritte.
```

Die automatische Auswahl ist aktiviert, aber kein garantierter Ausführungshook. Für eine verlässliche Beauftragung den Skill ausdrücklich nennen. Der Skill enthält Anweisungen, keinen eigenständig laufenden Scanner.

## Einordnung und Mitarbeit

Technische Prüfhilfe, keine Rechtsberatung oder Compliance-Zertifizierung. Zielmärkte, Nutzer und konkrete Funktionen bestimmen die Anwendbarkeit. Keine pauschalen Altersfelder oder automatischen Strafen pro Nutzer. Die Quellen sind datiert und müssen bei Anwendung aktuell geprüft werden; weitere Pflichten können außerhalb dieser sechs Bereiche liegen.

Issues und Pull Requests sind willkommen. Rechtliche Korrekturen bitte mit Primärquelle, Rechtsraum und Gültigkeitsdatum belegen; keine vertraulichen Daten veröffentlichen. Details unter [Contributing](README.md#contributing).

Veröffentlicht unter der [MIT-Lizenz](LICENSE).
