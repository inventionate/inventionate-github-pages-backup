---
layout: post
title: Archivist
subtitle: Offene und reproduzierbare Wissenschaft 
bigimg: [http://r-addict.com/images/fulls/github\_R.jpg][1]
---

Ab sofort stehen alle Datensätze, die ich im Rahmen meiner Dissertation generiere online zur Verfügung: [https://github.com/inventionate/zrs-data-repository][2]. 

Ich werde neben den Basisdaten auch Zwischenergebnisse publizieren. Dabei kann es sich sowohl um geometrische Modellierungen (MCA- oder HCPC-Objekte) als auch Diagramme handeln.

Um eine einfache Nutzung zu garantieren, greife ich auf das R Paket [archivist][3] zurück. Mit diesem wird [GitHub][4] in R integriert. Ich verstehe das als Beitrag zu einer _offenen_ und _reproduzierbaren Wissenschaft_.

Auf die Daten kann über folgenden Befehl zugegriffen werden: `loadFromRemoteRepo()`. Außerdem ist es mittels `cloneGitHubRepo()` möglich eine lokale Kopie der gesamten Repository anzulegen. Auf diese Art und Weise kann ggf. schneller auf die Artefakte zugegriffen werden.

[1]:	http://r-addict.com/images/fulls/github_R.jpg
[2]:	https://github.com/inventionate/zrs-data-repository
[3]:	http://r-addict.com/2016/06/13/RHero-Saves-Backup-City-With-archivist-github.html
[4]:	https://github.com