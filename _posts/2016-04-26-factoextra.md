---
layout: post
title: factoextra
subtitle: Visualisierung der Ergebnisse Geometrischer Datenanalysen
bigimg:
- "/img/fviz_mfa-1.png" : "Wolke der Individuen – Multiple Faktorenanalyse"
- "/img/fviz_mfa-2.png" : "Konzentrationsellipsen – Multiple Faktorenanalyse"
- "/img/fviz_mfa-3.png" : "Wolke der Subindividuen – Multiple Faktorenanalyse"
- "/img/fviz_mfa-1.png" : "Konfidenzellipsen — Multiple Faktorenanalyse"
---

Bei _factoextra_ handelt es sich um ein [R Paket][1], das 2015 von [Alboukadel Kassambara][2] entwickelt wurde.  Das Paket ermöglicht es die Ergebnisse multivariater Analyseverfahren zu extrahieren und zu visualisieren. Bei den unterstützten Verfahren handelt es sich um geometrische Verfahren (Hauptkomponentenanalyse, Multiple Korrespondenzanalyse, Clusterverfahren usf.). Insofern ist _factoextra_ ein ideales Werkzeug um _Geometrische Datenanalysen_ durchzuführen. Es eignet sich dafür besonders, weil es zur Visualisierung der Ergebnisse auf Hadley Wickhams [ggplot2][3] zurückgreift. Die generierten sind daher einfach an die individuellen Bedürfnisse anpassbar.

Seit Anfang 2016 darf ich als Mitentwickelt von _factoextra_ fungieren. Alboukadel bot mir erfreulicherweise diese Möglichkeit an, nachdem ich Funktionen zur Verarbeitung der Ergebnisse einer Multiplen Faktorenanalyse und einer Hierarchischen Multiplen Faktorenanalyse programmiert hatte. Damit unterstützt _factoextra_ nun alle klassischen (PCA, CA, MCA, HCPC) und einige erweiterte geometrische Verfahren (MFA, HMFA).

Sofern man [FactoMineR][4] zur Analyse verwendet sind alle Auswertungsstrategien in R umsetzbar, die Brigitte Le Roux und Henry Rouanet in ihrem wegweisenden Buch zur Geometrischen Datenanalyse vorschlagen (_Le Roux, B. & Rouanet, H., 2004. Geometric Data Analysis, New York: Kluwer_).

## Ein einfaches Beispiel

Anhand der Visualisierung der Ergebnisse einer Multiplen Korrespondenzanalyse soll das Potenzial einer Visualisierung mit _factoextra_ illustriert werden.

```r
# Pakete laden
library("FactoMineR")
library("factoextra")

Daten laden
data(poison)

# MCA berechnen
res.mca <- MCA(poison.active, graph=FALSE)

# Wolke der Individuen
fviz_mca_ind(res.mca, repel = TRUE, col.ind = "steelblue")
```

![][image-1]

Mit wenigen Zeilen lassen sich Konzentrationsellipsen in Abhängigkeit von _passiven Variablen_ plotten. Eine _Strukturierte Datenanalyse_ (Le Roux und Rouanet 2004), also die Interpretation der passiven Variablen als strukturierende Faktoren, ist auf einfache Art und Weise möglich.

```r
passive_variable <- as.factor(poison.active[, "Vomiting"])
p <- fviz_mca_ind(res.mca, label = "none", habillage = passive_variable,
	          addEllipses = TRUE, ellipse.level = 0.95)
print(p)
```

![][image-2]

## Umfangreiche Dokumentation

Seit kurzem existiert neben dem offiziellen [GitHub Repository][5] eine detaillierte Dokumentation: [http://www.sthda.com/english/rpkgs/factoextra/index.html][6]

Die GitHub Version von _factoextra_ lässt sich problemlos unter einer aktuellen R Version (3.2.4) installieren. Ab sofort steht das Paket auch über [CRAN][7] zur Verfügung.

[1]:	https://www.r-project.org
[2]:	http://alboukadel.com
[3]:	http://ggplot2.org
[4]:	http://factominer.free.fr/index.html
[5]:	https://github.com/kassambara/factoextra
[6]:	http://www.sthda.com/english/rpkgs/factoextra/index.html#
[7]:	https://cran.r-project.org/web/packages/factoextra/index.html

[image-1]:	/img/fviz_mca-1.png "Wolke der Individuen"
[image-2]:	/img/fviz_mca-2.png "Konzentrationsellipsen der passiven Variablen"
