Midterm-Special

Alle Schritte der Netzwerkerhebung

Überblick

Datenquelle: Episodenguide „Anne Will“ auf fernsehserien.de (Gästelisten der Folgen 500–503, Texte der ARD) Erhebungszeitraum der Sendungen: 20.02.2022 bis 13.03.2022 Netzwerktyp: gerichtet, two-mode (bipartit): Personen → Sendungen und Personen → Parteien Dateien: edgelist.csv, nodelist.csv Format: CSV, kommagetrennt, UTF-8, Kopfzeile vorhanden. Fehlende Werte sind leere Zellen. Nicht erfasst: die Moderatorin Anne Will (in allen Folgen anwesend, daher ohne Informationsgehalt für das Netzwerk) Folge Datum Titel

500: 20.02.2022 "Keine Entspannung im Konflikt mit Putin – wie ist ein neuer Krieg zu verhindern?" 501: 27.02.2022 "Putin führt Krieg in Europa – wie ist er zu stoppen?" 502: 06.03.2022 "Krieg gegen die Ukraine – wie weit wird Putin gehen?" 503: 13.03.2022 "Angriff auf die Ukraine – wie kann Putins Krieg beendet werden?"

Edgelist (edgelist.csv)

Jede Zeile ist eine gerichtete Kante von einer Person zu einer Sendung oder zu einer Partei.

from Beschreibung: ID des Ausgangsknotens (immer eine Person) Werte ID aus der Nodelist (Initialen)

to Beschreibung: ID des Zielknotens Werte: Sendungsnummer (500–503) oder Parteikürzel

relationship Beschreibung: Art der Beziehung Werte: 1 = nimmt als Gast an der Sendung teil; 2 = gehört der Partei an

Beispiel:

lk,500,1 lk,SPD,2

Lars Klingbeil war Gast in Folge 500 und gehört der SPD an.

Nodelist (nodelist.csv)

Jede Zeile ist ein Knoten. Es gibt drei Knotenarten: Personen, Parteien und Sendungen.

id Beschreibung; eindeutige Kennung des Knotens Werte: Personen: Initialen aus Vor- und Nachname in Kleinbuchstaben (lk); Parteien: Kürzel (CDU); Sendungen: Sendungsnummer (500)

name Beschreibung: Klarname Werte: Personenname, Parteiname oder Folge 500

party Beschreibung: Parteizugehörigkeit der Person Werte: CDU, SPD, FDP, GRUENE, LINKE, PvdA; leer = keine Partei genannt bzw. nicht erhoben

sector Beschreibung: gesellschaftlicher Bereich der Person Werte: Politik, Wissenschaft, Medien, Diplomatie, Militaer, Kultur; Parteiknoten: Partei; Sendungen leer

country Beschreibung: Land der Funktion bzw. Institution laut Gästeliste Werte: Deutschland, USA, Lettland, Niederlande, Ukraine

Kodierregeln und Hinweise

IDs:

Initialen aus Vor- und Nachname (Beispiel: Lars Klingbeil = lk). Adelsprädikate wie „von der“ oder „Graf“ werden ignoriert. Doppelte IDs wurden geprüft (alle 29 IDs sind eindeutig).

Sonderzeichen:

Umlaute und Sonderzeichen stehen nur in der Spalte name (z. B. Röttgen). In allen übrigen Spalten wurden sie umgeschrieben (GRUENE, Militaer).

Partei:

Erfasst ist die Parteizugehörigkeit, die in der Gästeliste der Sendung steht. Personen ohne Parteiangabe (Wissenschaft, Medien, Diplomatie, Militär, Kultur, Staatsoberhaupt) haben keine Kante zu einer Partei.

Ausnahme Frans Timmermans: In der Gästeliste steht keine Partei. Die Zuordnung zur niederländischen PvdA stammt aus eigener Recherche und ist keine Angabe der Quelle.

Ausnahme Egils Levits:

Staatspräsident Lettlands, in der Quelle ohne Parteiangabe, daher leer.

Ausnahme Egon Ramms:

General a. D., in der Quelle ohne Parteiangabe, daher leer.

Land:

Maßgeblich ist die in der Gästeliste genannte Funktion bzw. Institution. Constanze Stelzenmüller (Brookings Institution, Washington D.C.) ist daher mit USA kodiert. Ljudmyla Melnyk (Ukrainerin, Institut für Europäische Politik) und Katja Petrowskaja (deutsch-ukrainische Schriftstellerin) sind mit Deutschland kodiert.

Mehrfachteilnahme:

Wer in mehreren Folgen zu Gast war, hat mehrere Kanten 1 (Norbert Röttgen: 500, 501; Lars Klingbeil: 500, 503). Die Parteikante 2 steht nur einmal pro Person.

Gerichtet:

Alle Kanten laufen von der Person zur Sendung bzw. zur Partei.

Kennzahlen

29 Knoten: 19 Personen, 6 Parteien, 4 Sendungen 31 Kanten: 21 Teilnahmen (1) und 10 Parteizugehörigkeiten (2)
