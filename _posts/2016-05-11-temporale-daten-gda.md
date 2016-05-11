---
layout: post
title: Trajektorien visualisieren
subtitle: Längsschnittliche Daten geometrisch auswerten
bigimg: /img/trajectory-gda.jpg
---

Dieser Beitrag behandelt das Problem geometrischer Visualisierungen längsschnittlicher Daten. Um genau zu sein geht es darum, identische Daten, die an drei unterschiedlichen Zeitpunkten erhoben wurden, innerhalb eines Modells zu untersuchen. Die neueren Entwicklungen im Rahmen der Geometrischen Datenanalyse erlauben in diesem Fall bereits interessante Analysenstrategien anzuwenden. 

Sollen beispielsweise identische Konstrukte (Punktwolken), die auf Daten basieren, die zu unterschiedlichen Zeiten erhoben wurden, ist es möglich eine Meta-Analyse durchzuführen und diese temporal darzustellen. Sofern die Punktwolken das Ergebnis einer _Multiplen Korrespondenzanalyse_ sind, könnte beispielsweise eine _Multiple Faktorenanalyse_ berechnet werden. Diese ermöglicht es die partiellen Punkte der Einzelanalysen in einem Diagramm zu visualisieren. Da es sich bei den partiellen Punkten um Repräsentationen unterschiedlicher Zeitpunkte handelt, können diese durch Linien, bzw. Pfeile, verbunden werden. Das R Paket [FactoMineR][1] setzt diesen Ansatz durch die MFA-Option `chrono` um.
 
Ein etwas komplexeres Problem stellt sich, wenn die Modellierung der einzelnen Zeitpunkte bereits das Ergebnis _Multipler Faktorenanalysen_ sind. Gefragt ist dann eine "Meta-Meta-Analyse". Anders formuliert, es geht darum, sich zeitlich unterscheidende MFA-Resultate zu vergleichen.

Mein Lösungsansatz basiert darauf, die sogenannte _Hierarchische Multiple Faktorenanalyse_ zu verwenden. Dabei handelt es sich um eine Methodik, die neben unterschiedlichen Fragegruppen (MFA) auch die Hierarchie dieser Gruppen berücksichtigt. Der entscheidende Gedanke gründet darin, diese Hierarchie temporal zu begreifen. Anstatt eine inhaltliche Hierarchisierung vorzunehmen soll die HMFA einen Vergleich der unterschiedlichen MFA-Punktwolken visualisieren. Dadurch lassen sich sowohl Variationen der Antwortmuster als auch der Individuenpositionen bestimmen. Indem man die zuvor dargestellte Idee partieller Punkte aufgreift wird es überdies möglich Trajektorien zu visualisieren. Trajektorien, bzw. "Flugbahnen", beziehen sich dabei sowohl auf die individuelle Ebene als auch jene von Gruppen. Da es sich bei der HMFA um eine genuine Methode der Geometrischen Datenanalyse handelt, können alle Konzerte (Konzentrations- und Konfidenzellipsen, strukturierende Faktoren usf.) übertragen werden. Mittels der genannten Pfeile lassen sich demnach neben den Bewegungen einzelner Individuen auch Verlaufspfeile von Gruppen anzeigen. Die Interptretationsstringenz des statistisches Frameworks bleibt gewahrt. Die folgende Abbildung verdeutlicht diese Überlegungen anhand eines Ergebnisses, das mit der Funktion `fviz_gda_trajectory()` des [TimeSpaceAnalysis][2] Pakets generiert wurde.

![][image-1]

[1]:	http://factominer.free.fr
[2]:	https://github.com/inventionate/TimeSpaceAnalysis

[image-1]:	/img/trajectory-gda.jpg "Visualisierung vin Trajektorien"