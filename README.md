# LLKJJ-Knut: Buchhaltung + Steuererklärung für Künstler

Ein Django-basiertes Buchhaltungs- und Steuererklärungstool für freischaffende Künstler und Kleinunternehmer nach §19 UStG.

## 🎯 Projekt-Ziel

Umfassende Lösung für:
- **Buchhaltung** nach SKR03
- **Einnahme-Überschuss-Rechnung (EÜR)**
- **Steuererklärung** (ESt, GewSt)
- **Belegverwaltung** mit Dokumenten-Upload
- **ELSTER-Integration** (geplant)

## 🏗️ Technische Basis

- **Framework**: Django 5.2.3
- **Datenbank**: PostgreSQL (produktiv), SQLite (lokal)
- **Frontend**: Tailwind CSS + Django Templates
- **Code Quality**: ruff, mypy, black
- **Python**: 3.11+

## 📋 Funktionen

### ✅ Buchhaltung
- SKR03-Kontenrahmen
- Soll/Haben-Buchungssätze
- Geschäftspartner-Verwaltung
- Belegverwaltung (PDF, Bilder)

### 🔄 In Entwicklung
- EÜR-Generierung
- Steuererklärung (Anlage S/G)
- Automatische Kategorisierung
- ELSTER XML-Export

## 🚀 Installation & Setup

```bash
# Repository klonen
git clone https://github.com/Czok12/llkjj_knut.git
cd llkjj_knut

# Virtual Environment erstellen
python -m venv .venv
source .venv/bin/activate

# Dependencies installieren
pip install -r requirements.txt

# .env-Datei konfigurieren
cp .env.example .env
# .env bearbeiten mit eigenen Werten

# Datenbank migrieren
python manage.py migrate

# Entwicklungsserver starten
python manage.py runserver
```

## ⚠️ Wichtiger Hinweis

Dieses Tool ersetzt **keine Steuerberatung**. Bei steuerlichen Fragen immer einen Steuerberater konsultieren.

## 📝 Lizenz

MIT License - siehe LICENSE-Datei

## 🤝 Entwicklung

Entwickelt mit GitHub Copilot und Gemini AI-Unterstützung für optimale Code-Qualität.
- Keine Umsatzsteuerberechnung (Kleinunternehmerregelung)
- Fokus auf intuitive Bedienung und Automatisierung von Routineaufgaben

## Funktionsübersicht (geplant)
- SKR03-Kontenrahmen (Import, Verwaltung)
- Buchungen (Einnahmen, Ausgaben, Kontierung, Kategorien)
- Belegverwaltung (Upload, Verknüpfung mit Buchungen, Suche)
- Auswertungen (EÜR, Kontenblätter, Jahresübersicht)
- Steuerdokumente (Export, Vorlagen, Vorbereitung für Elster)
- Einstellungen (z.B. Kategorien, Konten, Nutzerprofil)

## Datenstrukturen (Basis)
- Konten (SKR03): Nummer, Name, Typ, Kategorie
- Buchung: Datum, Betrag, Konto Soll/Haben, Beleg, Kategorie, Beschreibung
- Beleg: Datei, Datum, Buchung, Notiz
- Nutzer: (nur 1, aber als Modell für spätere Erweiterung)

## Typische Workflows
1. Beleg erfassen (Upload/Foto, Metadaten eingeben)
2. Buchung anlegen (Einnahme/Ausgabe, Kontierung, Beleg zuordnen)
3. Auswertung/Jahresabschluss erstellen (EÜR, Übersicht)
4. Steuerdokumente vorbereiten/exportieren

## Besondere Regeln
- Keine USt-Ausweisung, keine UStVA
- Nur ein Mandant/Nutzer
- SKR03 als Kontenrahmen
- Datenhaltung lokal (kein Cloud-Zwang)

## Wünsche / Nice to have
- Automatische Kontierungsvorschläge
- Import von Bankumsätzen (CSV)
- Exportformate für Steuerberater/Elster
- Mobile Ansicht/Responsive Design

## Entwicklung
1. Virtuelle Umgebung aktivieren:
   ```zsh
   source .venv/bin/activate
   ```
2. Django-Server starten:
   ```zsh
   python manage.py runserver
   ```

## Hinweise
- Nur für einen Nutzer (Künstler, Kleinunternehmer)
- Keine Umsatzsteuerberechnung
- Fokus auf Übersichtlichkeit und einfache Bedienung
