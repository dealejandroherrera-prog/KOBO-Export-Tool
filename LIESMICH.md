# Browser-Version 7 – kompaktere Ansicht

## Öffnen
KoboNotes_Browser_v7.html wie bisher im Browser öffnen. Im Hosting-ZIP liegt dieselbe Datei als index.html. Vor dem Wechsel wichtige Exporte sichern: Bei unterschiedlichen lokalen HTML-Dateien kann der Browser getrennten Speicher verwenden. Der bisherige Speicherschlüssel bleibt kompatibel; ggf. Datenbank erneut importieren.

## Änderungen
- Sichtbares App-Branding, Versionsbanner und großer Einführungstext entfernt.
- Schlanker Titelbereich: „Bücher“ mit Bücherzahl auf der Hauptseite; Buchtitel und eine kleine Autorenzeile im Buch. Lange Titel werden einzeilig gekürzt; der vollständige Text bleibt im HTML und als Tooltip verfügbar.
- Feste untere Leiste auf eine Zeile reduziert. Auf dem Mac sind die Aktionen nebeneinander sichtbar. Auf schmalen Displays ist der Werkzeugbereich horizontal wischbar; Exportieren bleibt rechts fest erreichbar. Nicht alle Aktionen passen gleichzeitig auf ein iPhone. Die Schaltflächen behalten mindestens 44 Pixel Höhe. Die Leiste ist ohne iPhone-Sicherheitsabstand ungefähr 52–56 CSS-Pixel hoch.
- „Mit eigener Notiz“ liegt jetzt unten zwischen Gesamtauswahl und Verbinden. Im Buch ggf. in der unteren Werkzeugleiste seitlich wischen, um den Knopf zu erreichen.
- Kürzere Verbinden-Beschriftung („Verbinden“, aktiv „Beenden“), unveränderte Vorschau und Rückgängigmachen. Auswahlzähler und Alle auswählen/abwählen bleiben unten.
- Gesamtmarkierungszahl steht ganz oben in der Kapitelübersicht, vor Überschrift und Kapitelzeilen. Eigenständige Notizen werden weiter gesondert genannt. Zusammenführen verändert die ursprüngliche Markierungsanzahl nicht.
- Bücher als responsives Kartenraster: mehrere Karten nebeneinander am Mac, zwei auf mittleren Breiten und eine auf sehr schmalen Displays. Buchsymbol wählt aus; Titelbereich öffnet das Buch.
- Kapitelübersicht rechts bleibt erhalten; auf schmalen Displays oben, jetzt maximal 180 Pixel hoch und intern scrollbar.

## Bedienung bleibt erhalten
Kapitel anklicken filtert Markierungen; Zurück setzt Kapitel-/Such-/Notizfilter zurück. Alle auswählen/abwählen gilt weiterhin für das gesamte Buch bzw. die gesamte Bibliothek, nicht nur die gefilterten Treffer. Der Export richtet sich nach der gesamten Auswahl. Einzelne Karten werden per Klick farbig ausgewählt. Verbinden verwendet eine gesonderte Auswahl. Importhistorie und Neu-Kennzeichnung bleiben erhalten.

## Daten und Tests
Keine Änderung an der Kobo-Quelldatei und keine Daten-Uploads. Bestehende Import-/Seiten-/Speichergrenzen bleiben bestehen, einschließlich fehlender Verarbeitung separater WAL-/SHM-Dateien.
Automatisierte Logiktests mit synthetischer SQLite-Datenbank bestanden: Import, Buch-/Eintragsauswahl, Gesamtzahl oberhalb der Kapitel, Filter/Zurück, Notizfilter, Verbinden/Auflösen, Markdown und Speicherung. HTML-IDs, DOM-Verweise und Platzierung aller Aktionsknöpfe geprüft. Tests verwenden ein simuliertes DOM; das Layout wurde nicht in Safari oder auf einem echten iPhone visuell getestet. Bitte insbesondere die seitlich wischbare untere Werkzeugleiste auf dem iPhone prüfen.
