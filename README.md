# Auszählung

**Dieselben Stimmen, verschiedene Sieger.** Ein Stapel Stimmzettel liegt fest — und trotzdem hängt
der Gewinner am Auszählverfahren. Dieses Blatt rechnet das nicht an Anekdoten vor, sondern an
**allen 2002 möglichen Stapeln** mit drei Bewerbern und neun Wählern.

→ **[Blatt öffnen](https://ssims437.github.io/auszaehlung/)**

## Wer gewinnt

Fünf Vorlagen, vier Verfahren (relative Mehrheit, zwei Wahlgänge, übertragbare Stimme,
Borda-Punkte) und die vollständige Duellmatrix „jeder gegen jeden". Die Standardvorlage ist ein
Stapel, aus dem **drei Verfahren drei verschiedene Sieger** ziehen:

| Wähler | Reihung |
|---|---|
| 35 | A > C > B |
| 33 | B > C > A |
| 32 | C > B > A |

| Verfahren | Sieger | Stand |
|---|---|---|
| Relative Mehrheit | **A** | A 35 · B 33 · C 32 |
| Zwei Wahlgänge | **B** | nach Übertrag B 65 : A 35 |
| Übertragbare Stimme | **B** | C fliegt zuerst, seine Zettel gehen an B |
| Borda-Punkte | **C** | A 70 · B 98 · C 132 |
| Einzelvergleiche (Condorcet) | **C** | schlägt A mit 65:35 und B mit 67:33 |

Niemand hat betrogen, niemand hat sich verrechnet. Weitere Vorlagen: der **Condorcet-Zyklus** (A
schlägt B schlägt C schlägt A) und ein **Monotonie-Bruch**, den das Blatt beim Laden selbst sucht.

## Wie viele Sitze

Fünf Parteien, verstellbare Stimmen, Parlamentsgröße 5 bis 200 — verteilt nach **D'Hondt**,
**Sainte-Laguë**, **Hare-Niemeyer** und **Adams**, dazu die Abweichung vom rechnerischen Anspruch
und die Quotenbrüche. Der zweite Chart zeigt eine Partei über die wachsende Parlamentsgröße: bei
Hare-Niemeyer **verliert** sie zwischendurch Sitze, obwohl es mehr zu verteilen gibt
(Alabama-Paradox), bei D'Hondt nie.

## Was der Prüflauf zeigt

| Behauptung | Ergebnis |
|---|---|
| alle Stapel gezählt (3 Bewerber, 9 Wähler) | **2002 Stapel** · 112 ohne Condorcet-Sieger (5,6 %) |
| wie oft der Condorcet-Sieger übergangen wird | relative Mehrheit **10,9 %** · Borda 8,3 % · zwei Wahlgänge 3,1 % · übertragbare Stimme 3,1 % |
| relative Mehrheit ist schlechter als Borda | 206 gegen 156 Fälle |
| **Monotonie-Bruch der übertragbaren Stimme** | **gefunden**: Sieger C verliert gegen A, nachdem **ein** Wähler ihn von Platz 2 auf Platz 1 gehoben hat |
| Höchstzahlen = Divisorsuche | 1740 Fälle (3 Verfahren, 5 Stimmenbilder, 5–120 Sitze), keine Abweichung |
| **Gleichstand ist nicht auflösbar** | 262 von 348 Fällen ohne eindeutigen Divisor, 154 davon hängen an der Reihenfolge der Liste |
| Sitzsumme stimmt immer | 14 400 Verteilungen |
| Hare-Niemeyer hält die Quote, Divisoren nicht | 3720 Verteilungen · Quotenbrüche: Hare-Niemeyer **0** · D'Hondt **150** · Sainte-Laguë **1** |
| **Alabama-Fälle gesucht** | 40 Stimmenbilder, Parlament 1–150 · Hare-Niemeyer **252** Sitzverluste · D'Hondt **0** · Sainte-Laguë **0** |
| Sainte-Laguë liegt näher, D'Hondt bevorzugt die Größte | mittlerer Sitzfehler 0,263 gegen 0,337 · Aufschlag für die größte Partei: D'Hondt **+0,38** gegen Sainte-Laguë **−0,01** Sitze |
| Duellmatrix gegen einzeln abgezählte Zettel | 462 Stapel (6 Wähler) erschöpfend |

Zwei Zeilen sind **Suchzeilen**: sie sind bestanden, wenn ein Gegenbeispiel gefunden wird. Wäre
keines da, wäre die Erklärung im Blatt falsch — nicht das Verfahren gut.

## Was mich das gekostet hat

**168 von 1740 Sitzverteilungen wichen ab — und keine der beiden Rechnungen war falsch.** Die
Kreuzprobe stellt die Höchstzahlenrechnung (die im Wahlgesetz steht) gegen eine Divisorsuche (den
Blick von der anderen Seite). Sie widersprachen sich reihenweise, alle Fälle beim Stimmenbild
`500 000 / 100 000 / 100 000 / 100 000 / 100 000`:

| Verfahren | Sitze | Höchstzahlen | Divisorsuche |
|---|---|---|---|
| D'Hondt | 5 | 5/0/0/0/0 | 4/0/0/0/1 |
| D'Hondt | 8 | 5/1/1/1/0 | 4/1/1/1/1 |
| Adams | 118 | 66/13/13/13/13 | 65/14/13/13/13 |

Der Grund ist kein Rechenfehler, sondern ein **exakter Gleichstand**: bei vier gleich starken
Parteien springt die Summe der gerundeten Anteile über die Zielzahl (hier von 9 auf 4) — es gibt
**keinen** Divisor, der genau fünf Sitze ergibt. Beide Verfahren müssen dann irgendwie
nachjustieren, und wer den letzten Sitz bekommt, ist nicht berechenbar. Das Wahlgesetz sagt an
dieser Stelle: **das Los entscheidet.**

Die Konsequenz für den Prüflauf: die Kreuzprobe läuft jetzt auf Stimmenbildern **ohne** exakten
Gleichstand und muss dort auf den Sitz genau stimmen — und der Gleichstand ist eine eigene Zeile
geworden, die ihn als das ausweist, was er ist. Die Probe auf Willkür ist dabei die schönste
Messung des Blattes: dieselben Stimmen, nur die Parteien in umgekehrter Reihenfolge aufgeschrieben,
ergeben in **154 von 348 Fällen** eine andere Sitzverteilung. Es entscheidet die Liste, nicht die
Rechnung.

**Adams braucht eine Ausnahme, die in keiner Formel steht.** Bei den Höchstzahlen ist der Teiler für
Adams die Zahl der bereits erhaltenen Sitze — beim ersten Sitz also **null**. Ohne Sonderfall gibt
das eine Division durch null und damit `Infinity` für *alle* Parteien gleichzeitig; wer dann nach
„größter Wert" auswählt, gibt den ersten Sitz der Partei, die zufällig zuerst in der Liste steht.
Richtig ist: solange es Parteien ohne Sitz gibt, geht der Sitz an die stimmenstärkste davon. Das ist
kein Detail — es ist der Grund, warum Adams kleine Parteien bevorzugt: **jede** bekommt einen Sitz,
bevor die zweite Runde beginnt.

**Der Monotonie-Bruch war leichter zu suchen als von Hand zu bauen.** Ich wollte das Beispiel selbst
konstruieren und bin beim Nachrechnen jedes Mal in einen Gleichstand beim Ausscheiden gelaufen —
also in einen Fall, in dem nicht die Monotonie bricht, sondern die Tie-Break-Regel entscheidet.
Statt weiter zu basteln, sucht das Blatt jetzt selbst: alle 2002 Stapel, in jedem der Sieger, dann in jeder
Wählergruppe der Sieger um **einen Platz** angehoben, für jede mögliche Anzahl von Wählern. Das
kleinste Gegenbeispiel steht danach mit Zahlen da — und ist mit **einem einzigen** Wähler, der
seinen Favoriten von Platz 2 auf Platz 1 hebt, drastischer als das, was ich hinschreiben wollte.
Genau dafür ist der Rechner da: nicht um meine Beispiele zu bestätigen, sondern um bessere zu finden.

**Die Prozentzahlen sind ernüchternd unspektakulär.** Man erwartet, dass die relative Mehrheit
„ständig" den falschen Sieger wählt. Gemessen sind es **10,9 %** der Stapel mit eindeutigem
Condorcet-Sieger — jeder zehnte, nicht jeder zweite. Und die übertragbare Stimme, die für ihre
Monotonie-Brüche berüchtigt ist, übergeht ihn in nur **3,1 %**. Beide Zahlen sind gegen die eigene
Erwartung entstanden, und beide erklären, warum sich über Wahlverfahren so ausdauernd streiten
lässt: die Fehler sind selten genug, dass jeder aus Erfahrung recht behalten kann.

**Was das Blatt nicht kann:** Es kennt nur vollständige Reihungen ohne Gleichstand auf dem Zettel,
kein Zustimmungs- oder Bewertungswahlrecht, keine Wahlkreise, keine Sperrklauseln, keine
Überhangmandate und keine strategische Stimmabgabe (Gibbard-Satterthwaite steht in den Noten, wird
aber nicht durchgerechnet). Die erschöpfenden Läufe gehen bis drei Bewerber und neun Wähler; bei
vier Bewerbern gibt es 24 Reihungen, und die Zahl der Stapel wächst so schnell, dass „alle" nicht
mehr in einen Klick passt.

## Technik

Eine einzelne HTML-Datei. Kein Build, keine Bibliothek, nichts verlässt den Browser.
Canvas 2D, erschöpfende Aufzählung aller Stapel, hell und dunkel.

## Die ganze Sammlung

Alle Blätter nach Feld geordnet, jedes mit eigenem Repo:
**[ssims437.github.io](https://ssims437.github.io/)**

## Lizenz

MIT
