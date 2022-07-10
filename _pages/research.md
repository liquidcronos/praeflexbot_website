---
permalink: /research/
title: "Forschung"
layout: single
toc: true
---

In den nächsten Jahren grundsätzlich ist ein steigender Absatz elektrifizierter Fahrzeuge zu erwarten. Da die technische Entwicklung aber rasant weiter geht ist keine scharfe Prognose der Kundenanfrage und technischen Anforderungen möglich.
Um diesem Spannungsfeld zu begegnen, muss ein Wechsel von starren und unflexiblen Produktionssystemen zu höchstflexiblen Produktionsanlagen erfolgen.

Hier bieten sich Roboter an welche als Universalmaschinen eine große Reihe von Fertigungsprozessen abbilden können.
Im Gegensatz zu klassischen Werkzeugmaschinen haben Roboter allerdings eine deutlich geringere Präzision.

Dieses Projekt hat zum Ziel diese Gap zu schließen indem Robotersysteme durch hochgenaue optische Messsysteme erweitert werden und Konfigurations-,Bahn- und Trajektorienplanungstools entwickelt werden die hochpräzise Produktionsaufgaben befähigen.

Der Ansatz kann in zwei Schritten visualisiert werden

![initial_system](https://raw.githubusercontent.com/liquidcronos/praeflexbot_website/master/images/initial_system.png)
Im aktuellen State Of The Art, in diesem Fall exemplarisch ein Laserschweißprozess, fährt ein Roboter die ihm vorgegebene Trajektorie ab.
Da er keine Referenzmessung seiner Position zum Werkstück hat ist das Ergebnis relativ ungenau. 

![opt_ctr_system](https://raw.githubusercontent.com/liquidcronos/praeflexbot_website/master/images/opt_ctr_system.png)
Durch das zusätzliche Anbringen eines optischen Messystems kann die Präzision des Roboters stark erhöht werden da ungenau Positionierungen oder Kenntnis der Roboter Geometrie ausgeglichen werden.
Das Ergebnis ist aber nicht perfekt, den die Gelenke welche am Roboter gesteuert werden haben selbst nur eine endliche Präzision und so bleibt eine Streuung um die Ziel Koordinaten. Im nächsten Schritt soll der Einfluss dieser Streuung minimiert werden.

![double_opt_ctr](https://raw.githubusercontent.com/liquidcronos/praeflexbot_website/master/images/double_opt_ctr_system.png)

Der Einfluss der Gelenkpräzision auf die Präzision des Schweißprozesses hängt stark von der Konfiguration des Roboters ab.
Bei ausgestrecktem Arm wirkt sich ein kleiner Winkel Fehler an der Basis deutlich stärker aus als bei einem gefalteten Arm.

Im zweiten Schritt soll nun das Werkstück selbst so positioniert werden das der Schweißroboter immer in einer möglichst präzisen Konfiguration ist.
Da dies bei komplexen und großen Schweißbahn mehrfach passieren muss wird das Werkstück am Ende eines zweiten Roboterarms angebracht.

Zusammen mit dem optischen Messystem soll hier der absolute Positionsfehler als auch die Streuung minimiert werden.
Das Resultat ist eine deutlich präzisere Produktion der Zukunft. 

Mehr Informationen kann man auf dem [Projekt Onepager](https://www.icm.kit.edu/downloads/ICM-Projekte/ICM_Kurzvorstellung_SDManu3_SDPr%c3%a4FlexBot.pdf) finden.


---


