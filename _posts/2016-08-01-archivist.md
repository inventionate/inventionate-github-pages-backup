---
layout: post
title: Archivist
subtitle: Offene und reproduzierbare Wissenschaft 
bigimg: /img/archivist.jpg
---

Ab sofort stehen alle Datensätze, die ich im Rahmen meiner Dissertation generiere online zur Verfügung: [https://github.com/inventionate/zrs-data-repository][1]. 

Ich werde neben den Basisdaten auch Zwischenergebnisse publizieren. Dabei kann es sich sowohl um geometrische Modellierungen (MCA- oder HCPC-Objekte) als auch Diagramme handeln.

Um eine einfache Nutzung zu garantieren, greife ich auf das R Paket [archivist][2] zurück. Mit diesem wird [GitHub][3] in R integriert. Ich verstehe das als Beitrag zu einer _offenen_ und _reproduzierbaren Wissenschaft_.

Auf die Daten kann über folgenden Befehl zugegriffen werden: `loadFromRemoteRepo()`. Außerdem ist es mittels `cloneGitHubRepo()` möglich eine lokale Kopie der gesamten Repository anzulegen. Auf diese Art und Weise kann ggf. schneller auf die Artefakte zugegriffen werden.

[1]:	https://github.com/inventionate/zrs-data-repository
[2]:	http://r-addict.com/2016/06/13/RHero-Saves-Backup-City-With-archivist-github.html
[3]:	https://github.com