# Was hat ein Platz, was ein anderer nicht hat?

## Ergänzende Materialien zu Symmetrien bei zufälligen Anordnungen

## Python-Simulationen

Die Python-Notebooks können ohne Installation direkt im Browser geöffnet,
verändert und ausgeführt werden.

[![JupyterLite](https://jupyterlite.rtfd.io/en/latest/_static/badge.svg)](https://rveh.github.io/symmetrie-stochastik/jupyterlite/lab/index.html?path=00_Start.ipynb)

[![Binder](https://mybinder.org/badge_logo.svg)](
https://mybinder.org/v2/gh/RVeh/symmetrie-stochastik/HEAD?urlpath=lab/tree/python/00_Start.ipynb)


Dieses Repository enthält die digitalen und vertiefenden Materialien zum
Beitrag

> Norbert Henze und Reimund Vehling: *Was hat ein Platz, was ein anderer
> nicht hat? – Symmetrie bei zufälligen Anordnungen von Objekten aus zwei
> Klassen.*

Ausgangspunkt sind $w$ weiße und $s$ schwarze Kugeln, die ohne
Zurücklegen gezogen und dadurch zufällig auf $N=w+s$ Positionen
angeordnet werden.

Die theoretischen Symmetrieargumente stehen im Zentrum des Beitrags. Die
digitalen Materialien eröffnen dazu eigenständige experimentelle
Erkenntniswege: Sie machen Invarianten und Streuung sichtbar, führen zu
Vermutungen und ermöglichen die Kontrolle exakter Ergebnisse.

> Die Simulation lässt die Gleichberechtigung der Positionen sichtbar
> werden, die Kombinatorik bestätigt sie exakt – die Symmetrie erklärt
> sie.

## GeoGebra

### Positionen

Die Datei untersucht für jede Position $j$ die relative Häufigkeit
$h(A_j)$ einer weißen Kugel. Im Mittelpunkt steht die Leitfrage:

> Was bleibt bei jeder neuen Simulation gleich – und was stabilisiert
> sich erst bei vielen Wiederholungen?

Bei jeder Simulation gilt bereits exakt

$$
\frac{h(A_1)+\dots+h(A_N)}{N}=\frac{w}{N},
$$

während sich die einzelnen Werte $h(A_j)$ erst mit wachsender
Wiederholungszahl bei $w/N$ stabilisieren. Dadurch werden die
unterschiedlichen Erkenntnisfunktionen von Simulation, Kombinatorik und
Symmetrie sichtbar. Zugleich führt die Untersuchung zur Frage, was die
Gleichberechtigung der Positionen für die eigene Entscheidung vor einem
einzigen Versuch bedeutet.

### Lückenlängen

Die $w$ weißen Kugeln erzeugen $w+1$ Lücken für die $s$ schwarzen
Kugeln: vor, zwischen und nach den weißen Kugeln. Die Datei führt von
einer einzelnen Farbfolge über die Lückenlängen zu einer Datenmatrix für
viele Realisationen. Empirische Mittelwerte und Standardabweichungen
machen die Gleichberechtigung, aber auch die erhebliche Streuung der
Lückenlängen sichtbar.

Zu beiden Dateien gehören ausführliche Erläuterungen der mathematischen
Modellierung, der GeoGebra-Befehle und ihrer didaktischen Funktion.

## Python-Notebooks

Der Binder-Start führt zunächst zur
[Übersicht der Python-Programme](00_Start.ipynb).

| Notebook | Inhalt |
| --- | --- |
| [Simulation_Urne_ohne_Zuruecklegen.ipynb](python/Simulation_Urne_ohne_Zuruecklegen.ipynb) | Relative Häufigkeiten \(h(A_j)\), exakte Invariante, Stabilisierung, bedingte Wahrscheinlichkeiten und hypergeometrischer Ausblick |
| [Simulation_erwartete_Positionen.ipynb](python/Simulation_erwartete_Positionen.ipynb) | Positionen \(T_j\) der weißen Kugeln, empirische Erwartungswerte, Varianzen und Standardabweichungen sowie Spiegelsymmetrie |
| [Simulation_Luecken.ipynb](python/Simulation_Luecken.ipynb) | Empirische und exakte Verteilung einer Lückenlänge, Erwartungswert, Varianz, Standardabweichung und punktweise Wilson-Konfidenzintervalle |

Alle veränderbaren Eingaben stehen jeweils am Anfang eines Notebooks.
Die Voreinstellung `seed = 42` macht die Simulationen reproduzierbar.

## Weitergedacht

Das vertiefende Material greift Beobachtungen auf, die beim Arbeiten mit
der einfachen Positionssimulation entstanden sind. Es führt von der
Invariante über die erwartete Zahl verschiedener Farbfolgen

$$
E(D_m)
=M\left(1-\left(1-\frac1M\right)^m\right),
\qquad
M=\binom{N}{w},
$$

bis zur Verbindung mit dem Rencontre-Problem. Der Erkenntnisweg zeigt
exemplarisch, wie aus Beobachten, Fragen, Strukturieren, Begründen und
Verallgemeinern neue Mathematik entsteht – auch in der Schule.

## Python lokal ausführen

Vorausgesetzt wird Python 3.11. Danach genügen im Repository:

```bash
python -m pip install -r requirements.txt
jupyter lab
```

Eine lokale Installation ist für die Nutzung jedoch nicht erforderlich:
Der Binder-Link am Anfang dieser Seite startet die Notebooks direkt im
Browser. Beim ersten Aufruf kann der Aufbau der Umgebung einige Minuten
dauern.
