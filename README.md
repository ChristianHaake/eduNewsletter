# eduNewsletter

> Ein automatisierter, KI-gestützter und kuratierter Newsletter, der aktuelle Fachartikel, digitale Unterrichtsmaterialien und relevante Informationen für Lehrkräfte bündelt.

Dieses Projekt aggregiert Bildungsnachrichten über RSS-Feeds, nutzt Künstliche Intelligenz zur Filterung, Verschlagwortung (Tagging) und Zusammenfassung und stellt die Ergebnisse über eine Open-Source-Infrastruktur bereit.

* **Website:** [edunewsletter.haak3.de](https://edunewsletter.haak3.de) (zukünftig *eduNewsletter.de*)
* **Plattform:** Ghost (Self-hosted)
* **Repository:** [github.com/ChristianHaake/eduNewsletter](https://github.com/ChristianHaake/eduNewsletter)

---

## Inhaltsverzeichnis
* [Über das Projekt](#über-das-projekt)
* [Nutzen für Lehrkräfte](#nutzen-für-lehrkräfte)
* [Technische Funktionsweise (Architektur)](#technische-funktionsweise-architektur)
* [KI-Transparenzerklärung (AI Transparency)](#ki-transparenzerklärung-ai-transparency)
* [Nutzung und Abonnement](#nutzung-und-abonnement)
* [Projektstruktur (Repository-Übersicht)](#projektstruktur-repository-übersicht)
* [Mitwirken](#mitwirken)
* [Lizenz](#lizenz)

---

## Über das Projekt
Lehrkräfte stehen vor der Herausforderung, digitale Materialien und aktuelle Informationen zeiteffizient für den Unterricht zu finden. Dieses Projekt automatisiert die Sichtung von Bildungsmedien, strukturiert die Daten und bereitet sie für die Schulpraxis auf.

## Nutzen für Lehrkräfte
* **Zeitersparnis:** Reduziert den Rechercheaufwand für die Unterrichtsvorbereitung durch gezielte Vorfilterung.
* **Fokus auf Relevanz:** KI-gestütztes Tagging ermöglicht das schnelle Finden von passenden Themen der Schul- und Unterrichtsentwicklung.
* **Dauerhafter und offener Zugriff:** Alle Newsletter-Ausgaben bleiben im GitHub-Archiv als Markdown-Dateien frei zugänglich, durchsuchbar und plattformunabhängig bestehen.

---

## Technische Funktionsweise (Architektur)

Das System basiert auf einer dreistufigen Pipeline, um maximale Automatisierung bei voller redaktioneller Kontrolle zu gewährleisten:

[ RSS-Feeds ] ──> [ KI-Pipeline ] ──> [ Ghost Blog ] ──> [ Newsletter ]
│ (Filter, Tag,     (Self-hosted)
└─ Zusammenfassung)      │
▼
[ GitHub-Archiv ]


1. **Aggregation:** Relevante Blogs, Ministerien und OER-Plattformen werden kontinuierlich über RSS-Feeds eingelesen.
2. **KI-Verarbeitung:** Ein lokales/KI-gestütztes System filtert irrelevante Beiträge heraus, vergibt thematische Tags und generiert prägnante, sachliche Zusammenfassungen.
3. **Kuration & Versand:** Die aufbereiteten Entwürfe werden in die self-hosted Ghost-Instanz übertragen. Nach der manuellen Endkontrolle erfolgt die Veröffentlichung auf der Website und der Versand als E-Mail-Newsletter. Parallel wird eine Kopie als Markdown im GitHub-Archiv gesichert.

---

## KI-Transparenzerklärung
Im Bildungsbereich ist ein verantwortungsvoller Umgang mit Automatisierung essenziell. Dieses Projekt nutzt Künstliche Intelligenz (KI) als Assistenzwerkzeug, nicht als finalen Entscheider.

* **Automatisierte Vorarbeit:** Die Vorab-Recherche, das Auslesen der RSS-Feeds, das Vergeben von Schlagworten (Tags) sowie das Erstellen der ersten Textzusammenfassungen erfolgen KI-gestützt.
* **Menschliche Qualitätskontrolle (Human-in-the-Loop):** Kein Text wird ungeprüft veröffentlicht. Jede Ausgabe durchläuft eine manuelle redaktionelle Prüfung. Zusammenfassungen werden auf Richtigkeit kontrolliert, stilistisch angepasst und final kuratiert.
* **Quellenehrlichkeit:** Die Originalquellen und Urheberrechte der aggregierten Artikel und Unterrichtsmaterialien werden in jeder Ausgabe transparent ausgewiesen.

---

## Nutzung und Abonnement
* **Per E-Mail & Web:** Die Anmeldung zum kostenlosen Newsletter sowie alle bisherigen Blogbeiträge finden Sie auf [edunewsletter.haak3.de](https://edunewsletter.haak3.de).
* **Über GitHub:** Direkter, plattformunabhängiger Zugriff auf den Quellcode und das Beitragsarchiv in diesem Repository.

---

## Projektstruktur (Repository-Übersicht)
* `/archiv`: Enthält alle versendeten Newsletter-Ausgaben als reine Markdown-Dateien.
* `/config`: Konfigurationsdiele (z. B. `sources.md`) für die automatische Quellensynchronisation.
* `/src`: Skripte für die KI-Pipeline (Aggregation, API-Anbindung, Ghost-Schnittstelle).

---

## Mitwirken
Hinweise auf Fehler, Vorschläge für neue RSS-Quellen oder Optimierungen an der Prompt-Struktur für die Zusammenfassungen können direkt über die *Issues* eingereicht werden.

## Lizenz
Die Inhalte und Skripte dieses Repositories stehen unter der [z. B. CC BY 4.0 / MIT] Lizenz.
