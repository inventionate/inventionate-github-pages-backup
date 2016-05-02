---
layout: post
title: Zeitmuster im Wintersemester 2015/2016
subtitle: Berechnungen und Ergebnisse
bigimg: /img/zeitmuster.jpg
---

Zur Erhebung und Analyse studentischer Zeitbudgets existieren bereits einige Untersuchungen. Neben den Befunden der großen bundesdeutschen Vergleichsstudien des [DZHW][1] (z. B. Sozialerhebung) und der [AG Hochschulforschung][2] (Studierendensurvey) hat insbesondere die Studie von Rolf Schulmeister und Christiane Metzger, _Die Workload im Bachelor: Zeitbudget und Studierverhalten (2011)_ für einiges Aufsehen gesorgt. Entgegen dem medialen Trend attestieren die Autor/innen den Bachelorstudierenden nämlich keineswegs eine Überforderung und einen stressigen Studienalltag. Vielmehr konnten sie feststellen, "dass die Zeit, die die Studierenden in das Studium investieren, im Mittel viel geringer ist als von früheren Befragungen ermittelt und weit unter den von Bologna und den Modulhandbüchern geforderten Werten liegt" (Vorwort). Es formiert sich kein allzu freundliches Bild der heutigen Studierendenschaft. Allerdings lohnt es sich weiter zu lesen. Schulmeister und Metzger kommen nämlich zu "noch wichtigeren" Ergebnissen. Demnach sei die Streuung der studienrelevanten Zeitverwendungen enorm. Man müsse von einer großen Heterogenität ausgehen, die zugleich keinen kausalen Zusammenhang zwischen Studienerfolg und Zeitaufwand erlaube. Von größerer Bedeutung sei das Zeitbewusstsein, bzw. ein reflexiver Umgang mit Zeit. Oft würden gerade jene Studierenden, die subjektiv über großen Belastungen klagen, eine vergleichsweise geringe objektive Lernzeit aufweisen (vgl. Vorwort).

Ausgehend von diesen punktuellen Einblicken in den hochschulübergreifenden Diskurs werde ich im Folgenden erste Ergebnisse der Zeit-Raum Studium Befragung an der PH Karlsruhe im Wintersemester 2015/2016 präsentieren. Nach einer methodischen Darstellung folgt die Diskussion von vier Zeitmuster, die rekonstruiert werden konnten.

## Die Analysemethode 

Das Grundproblem der Aggregation von Zeitbudget-Daten besteht darin, dass diese in Abhängigkeit von zwei Eigenschaften geclustert werden müssen (vgl. Studer, M., 2014. WeightedCluster Library Manual). Sowohl von der Dauer einer Tätigkeit als auch ihrer kalendarischen Verortung. Ob man dienstags oder samstags vier Stunden am Stammtisch verbringt ist ein gewichtiger Unterschied, der in der Analyse berücksichtigt werden soll.

![][image-1]

Um diesem Umstand Rechnung zu tragen, wurden die Zeitprofile mit Hilfe des _kml3d Algorithmus_ berechnet (Genolini, C. et al., 2015. kml and kml3d: R Packages to Cluster Longitudinal Data. Journal of Statistical Software, 65(4)). Das Bild oben visualisiert das Vorgehen. Die Zeitbudgets werden als Funktionen betrachtet, die für jede Tätigkeit, in diesem Fall sieben verschiedene, bestimmt werden. Bis zu diesem Punkt könnte ein klassischer kml-Algorithmus eingesetzt werden. Das heißt, pro Aktivität ließen sich nun Gruppen bilden. Da die Zeitprofile allerdings über alle Tätigkeiten hinweg gebildet werden sollen, wird kml3d eingesetzt. Dieser berücksichtigt neben dem Verlauf der Funktion, also der Dauer einer Tätigkeit (y-Achse) und deren kalendarischer Verortung (x-Achse), die Funktionsverläufe aller anderer Tätigkeiten.

Ausreißer, die in der Regel mit fehlerhaft ausgefüllten Erhebungstabellen zusammenhängen, beeinflussen den Algorithmus nur minimal, was an den sinnlosen Linien bei "Schlafen" und "Freizeit" zu erkennen ist. Datensätze, die zu stark kompromittiert sind, wenn sie etwa zu viele fehlende Werte aufweisen, werden von der Analyse ausgeschlossen.

## Ergebnisse

Das Ergebnis der Clusterbildung sind vier Gruppen. Jede Gruppe unterscheidet sich anhand einer Tätigkeit von den anderen. Die insbesondere im ersten Semester strukturell vorgegebenen Veranstaltungstermine haben, wenig überraschend, zu keiner besonderen Profilierung geführt. Das gleiche gilt für die Zwischenzeit, die sich auf die Zeitspannen zwischen Veranstaltungen bezieht. Auch die Angaben zum Schlaf unterscheiden sich allenfalls marginal.

Anders sieht es in Bezug auf die vermutete Freizeit aus. Eine große Gruppe von Studierenden (36,6%) gab einen deutlich höheren Wert als alle anderen Studierenden an (rotes Zeitmuster). Das zweitgrößte Zeitmuster (28,7%) bilden Personen, die einen vergleichsweise großen Selbststudienanteil ausgewiesen haben (blau). Erwerbstätige, die vor allem am Wochenende einer bezahlten Arbeit nachgehen, bilden das dritte Zeitmuster (19,6%). Ein fünftel Aller Studienanfänger/innen arbeitet demnach, um das Studium zu finanzieren. Die im Vergleich kleinste Gruppe bilden die Pendler/innen (15,1%, violett).

![][image-2]

das Bild stellt die vier Zeitprofile als übersichtliches Zeitmuster dar, an dem die Unterschiede nochmals abgelesen werden können. Auf der x-Achse sind die Wochentage abgetragen, die y-Achse visualisiert die prozentuale Verteilung der Aktivitäten. Das erste Zeitprofil unterscheidet sich durch einen wesentlich umfangreichen grünen Anteil (Freizeit). Demgegenüber weist das zweite Profil einen vergleichsweise großen hell-orangen Anteil auf (Selbststudium). Profil drei sticht durch eine überdurchschnittlich umfangreiche Arbeitszeit (gelb) hervor. Zuletzt können die Pendler/innen durch einen großen Anteil hellgrün identifiziert werden. Die Bilder machen zudem deutlich, dass die Angaben zu Veranstaltungen (rot) und Schlafen (blau) keine nennenswerten Differenzen ausweisen.

[1]:	http://www.dzhw.eu
[2]:	https://cms.uni-konstanz.de/ag-hochschulforschung/startseite/

[image-1]:	/img/zeitmuster_zeitserien.jpg "Die Klassifikation von Zeitmustern"
[image-2]:	/img/zeitmuster_durchschnittliche_clusterprofile.jpg "Die vier durchschnittlichen Zeitprofile"