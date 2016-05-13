---
layout: post
title: Trajektorien anders gedacht
subtitle: Passive Individuen als Ausgangspunkt
bigimg: /img/trajectory-gda-2.jpg
---

Im Anschluss an meine Bemühungen "Trajektorien" im Rahmen Geometrischer Datenanalysen zu visualisieren habe ich in meinem letzten Post eine Möglichkeit dargelegt, wie zeitliche Veränderungen mittels _partieller Individuenpunkte_ konstruiert werden können. Dabei wird ein _Differenzraum_ konstruiert, der im Sinne der Geometrischen Datenanalyse auf _aktiven Variablen_ basiert. Auch wenn dieses Vorgehen einige Vorteile bietet handelt man sich damit auch einige "Probleme" ein. Diese beziehen sich insbesondere auf die Darstellung der Ergebnisse. Da die konstruierte Punktwolke auf neuen Variablen basiert, erhält man neben der Möglichkeit Trajektorien nachzuzeichnen auch eine neue Anordnung der Variablen, die es zu interpretieren gilt. Zwar lassen sich damit differenziertere Aussagen über die zeitliche Variation treffen, allerdings muss die Modifikation des Gesamtmodells ausgeführt werden.

Insofern ist es ggf. vorteilhaft die zeitlich divergenten Variablen auf das bereits bekannte Modell des ersten Erhebungszeitpunkts zu beziehen. Indem die später erhobenen Daten als _passive Individuen_ integriert werden, kann deren positionale Veränderung in Bezug zu den Ausgangsdaten sichtbar gemacht werden. Dabei handelt es sich um Antwortmuster (Individuen), die bei der Konstruktion des Modells nicht berücksichtigt werden. Auf diese Weise wird das Modell nicht geändert, die Position der zusätzlichen (passiven) Individuen kann aber trotzdem bestimmt werden. Das gleiche Prinzip wird bei [Locate!][1] genutzt. Diese Analysestrategie wird beispielsweise auch von Jörg Blasius zur Analyse von Paneldaten empfohlen (_Blasius, J., 2001. Korrespondenzanalyse, Oldenbourg, München/Wien_).

Um auf dieser Grundlage Trajektorien zu visualisieren müssen lediglich die jeweiligen Individuen relationiert werden. Das heißt, jedem aktiven Individuen (Erhebungszeitpunkt 1) werden die entsprechenden passiven Individuen der folgenden Erhebungszeitpunkte zugeordnet. Sobald das geschehen ist, können die einzelnen Punkte durch Linien und/oder Pfeile verbunden werden. 

![][image-1]

Die Ergebnisse dieses Vorgehens wirken zunächst identisch zu jenen, die auf einer MFA oder HMFA aufbauen. Allerdings können die vorhergehenden Interpretation direkt übertragen werden. Beispielsweise lassen sich – wie im Beispiel geschehen – die jeweiligen Achsenbezeichnungen eintragen. Durch die zusätzlichen passiven Individuen hat sich an der Anordnung der Antworten nichts geändert.

Der Plot wurde mit der Funktion `fviz_gda_trajectory()` des [TimeSpaceAnalysis][2] Pakets erstellt. Die Funktion ermöglicht über die Visualisierung hinaus die Filterung der Ergebnisse. Im angeführten Bild wurden lediglich die zehn am stärksten variierenden Personen eingezeichnet und in Abhängigkeit der Ergebnisse einer _Hierarchischen Clusteranalyse der Hauptkomponenten_ (HCPC) abgebildet. Die Filterung der Ergebnisse erlaubt differenzierte Analysen. Ähnlich der HMFA Umsetzung sind zudem gruppenspezifische Untersuchungen mittels Konzentrationsellipsen möglich. 

[1]:	http://rapps.ph-karlsruhe.de/users/fmundt/Locate/
[2]:	https://github.com/inventionate/TimeSpaceAnalysis

[image-1]:	/img/studienalltag-trajektorien-pi.jpg "Trajektorien passiver Individuen"