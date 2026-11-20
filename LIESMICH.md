# Browser-Version 9 – Bücher zusammenführen

## Bedienung
1. Auf der Hauptseite mindestens zwei Bücher über ihre Buchsymbole auswählen.
2. Unten „Bücher zusammenführen“ wählen.
3. Titel und Autor jeweils aus einer Quelle auswählen. Unterschiedliche Angaben müssen ausdrücklich gewählt werden; identische Angaben sind vorgewählt. Titel und Autor dürfen aus verschiedenen Quellen stammen.
4. Vorschau prüfen und „Akzeptieren“ drücken. Abbrechen verändert nichts.
5. Die ursprünglichen Steckbriefe werden lokal durch einen gemeinsamen ersetzt. Alle Einträge bleiben erhalten, einschließlich ausgeschlossener Einträge, Textnotizen, Datumsangaben und Favoriten.
6. Im gemeinsamen Steckbrief kann „Zusammenführung lösen“ die ursprünglichen Bücher wiederherstellen.

## Stammdaten und Quellen
Die aktuelle App liest Titel und Autor; nur diese Felder werden abgeglichen. Quell-IDs bleiben intern erhalten. ISBN, Verlag, Sprache und Cover werden nicht erfunden.
Kapitel bleiben nach Quellbuch getrennt, auch bei gleichen Titeln. Quelle wird im Kapiteltitel der Übersicht und im Markdown sowie klein in den Zitaten angezeigt. Alle Zitate werden übernommen; gleiche Textpassagen aus verschiedenen Ausgaben werden nicht automatisch gelöscht. Identische doppelte Eintrags-IDs werden als Konflikt abgelehnt.
Bestehende Zitatverbindungen bleiben erhalten. Einzelzitate können nicht über Quellbuchgrenzen hinweg verbunden werden. Bereits zusammengeführte Bücher können mit weiteren Büchern zusammengeführt werden; Auflösen stellt alle ursprünglichen Quellen her.
Die bisherige Buchauswahl aktiviert beim Auswählen eines ganzen Buchs dessen Einträge. Dies ist unverändert; Zusammenführen selbst verändert Eintragsausschlüsse nicht. Der neue Steckbrief ist für den Sammel-Export ausgewählt.

## Speichern und erneuter Import
Gruppen, gewählte Stammdaten und Originalquellen werden lokal im bisherigen Browserspeicher gespeichert. Die gewählten Titel-/Autorwerte werden bei erneutem Import nicht ungefragt überschrieben.
Beim erneuten Import werden alle Quellen aktualisiert und die Gruppe wiederhergestellt, wenn sämtliche Quell-IDs vorhanden sind. Neue Zitate kommen hinzu. Fehlt eine Quelle, wird die Gruppe aufgelöst und eine Warnung über nicht wiederhergestellte Verbindungen angezeigt. Zitate fehlender Quellen werden nicht als alte Kopien behalten.
Speicherfehler beim Akzeptieren oder Auflösen setzen den jeweiligen Änderungsschritt zurück. Browserbereinigung entfernt die gespeicherten Gruppen. Keine Synchronisierung zwischen Geräten. Quelldatei auf dem Kobo unverändert.

## Start und Hosting
KoboNotes_Browser_v9.html öffnen. Für GitHub Pages index.html aus dem Hosting-ZIP im vorhandenen Repository ersetzen. Keine persönliche Kobo-Datenbank hochladen. Unterschiedliche lokale HTML-Dateien können getrennten Browserspeicher haben. Vor Updates wichtige Exporte sichern; möglichst dieselbe HTTPS-Adresse weiterverwenden.

## Teststatus
JavaScript-Syntax und automatisierte Tests bestanden: Stammdatenwahl, Akzeptieren/Abbrechen, Quellen/Kapitel, Erhalt der Zitate und Notizen, Favoriten/Ausschlüsse, Speichern/Laden, erneuter Import, fehlende Quelle, Auflösen, Speicherfehler und bestehende Zitatverbindungen. HTML-IDs/DOM-Verweise geprüft. UI-Tests mit simuliertem DOM, kein visueller Safari-/iPhone-Test. Keine Prüfung deiner persönlichen Datenbank. Bisherige Grenzen bezüglich SQLite-Snapshots/WAL und Seitenangaben bleiben bestehen.
