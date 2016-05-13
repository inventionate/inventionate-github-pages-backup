---
layout: post
title: Trajektorien visualisieren
subtitle: Längsschnittliche Daten geometrisch auswerten
bigimg: /img/trajectory-gda.jpg
---

Dieser Beitrag behandelt das Problem geometrischer Visualisierungen längsschnittlicher Daten. Um genau zu sein geht es darum, identische Daten, die an drei unterschiedlichen Zeitpunkten erhoben wurden, innerhalb eines Modells zu untersuchen. Die neueren Entwicklungen im Rahmen der Geometrischen Datenanalyse erlauben in diesem Fall bereits interessante Analysenstrategien anzuwenden. 

Sollen beispielsweise inhaltlich identische, zeitlich divergente Punktwolken verglichen werden, ist es möglich eine Meta-Analyse durchzuführen und die temporale Differenten abzubilden. Sofern es sich bei den partiellen Punktwolken und die Resultate von _Multiplen Korrespondenzanalysen_ (kategoriale Daten) oder von _Hauptkomponentenanalysen_ (metrische Daten) handelt, kann eine _Multiple Faktorenanalyse_ berechnet werden. Die partielle Indivsiuenpositionen der Einzelanalysen lassen sich dann in einem Gesamtdiagramm visualisieren. Pagès bezeichnet diese Visualisierung als _star plot_ (_ Pagès, J., 2015. Multiple Factor Analysis by Example Using R. Boca Raton: CRC_). Da es sich im Fall längsschnittlicher Daten bei den partiellen (Individuen)Punkten um Repräsentationen unterschiedlicher Zeitpunkte handelt, können diese durch Linien, bzw. Pfeile, verbunden werden. Das R Paket [FactoMineR][1] setzt diesen Ansatz durch die Option `chrono` der Funktion `plot.MFA` um.
 
Ein etwas komplexeres Problem stellt sich, wenn die zeitlich divergenten Punktwolken bereits das Ergebnis von _Multiplen Faktorenanalysen_ sind. Gefragt ist dann eine "Meta-Meta-Analyse". Anders formuliert, wie können inhaltlich identische, zeitlich variierende MFA-Resultate verglichen werden?

Mein Lösungsansatz basiert darauf, die sogenannte _Hierarchische Multiple Faktorenanalyse_ (HMFA) zu verwenden. Dabei handelt es sich um eine Methodik, die neben unterschiedlichen Variablengruppen auch deren hierarchische Relationen berücksichtigt. Der entscheidende Gedanke gründet darin, die abgebildete Hierarchie temporal zu begreifen. Anstatt eine inhaltliche Hierarchisierung vorzunehmen, soll die HMFA einen Vergleich der unterschiedlichen MFA-Punktwolken visualisieren. Dadurch lassen sich sowohl Variationen der Antwortmuster als auch der Individuenpositionen bestimmen. Indem man die zuvor dargestellte Idee partieller (Individuen)Punkte aufgreift wird es überdies möglich _Trajektorien zu visualisieren_. Trajektorien, bzw. "Flugbahnen", beziehen sich dabei sowohl auf die individuelle Ebene als auch die Gruppenebene. Da es sich bei der HMFA um eine genuine Methode der Geometrischen Datenanalyse handelt, können nahezu alle geometrischen Konzepte (Konzentrations- und Konfidenzellipsen, strukturierende Faktoren usf.) übertragen werden. Mittels der genannten Pfeile lassen sich daher neben den Bewegungen einzelner Individuen auch Verlaufspfeile von Gruppen anzeigen. Die Interpretationsstringenz des statistischen Frameworks bleibt gewahrt. Die folgende Abbildung verdeutlicht diese Überlegungen anhand eines Ergebnisses, das mit der Funktion `fviz_gda_hmfa_trajectory()` des [TimeSpaceAnalysis][2] Pakets generiert wurde.

![][image-1]

[1]:	http://factominer.free.fr
[2]:	https://github.com/inventionate/TimeSpaceAnalysis

[image-1]:	/img/trajectory-gda.jpg "Visualisierung vin Trajektorien"