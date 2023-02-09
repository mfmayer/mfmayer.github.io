---
title: Wärmepumpe
description: Informationen zu meiner Wärmepumpe *Buderus WPL6 IK* und wie ich sie optimierte
#date: 2023-01-18T19:11:01.499Z
#lastmod: 2023-01-19T16:21:45.241Z
draft: false
tags:
  - ""
---

Das aus meiner Sicht größte Problem mit Wärmepumpen ist, dass sie irgendwer auch entsprechend konfigurieren sollte. Oft werden die Wärmepumpen aber wohl nur schnell aufgestellt, an die Fußbodenheizung angeschlossen, größtenteils Voreinstellungen übernommen und die Thermostaten in den Zimmern sollen den Rest erledigen. Das funktioniert auch, aber meistens weder effizient noch Materialschonend.

## Grundlagen

Die folgende stark vereinfachte Darstellung zeigt den Vor- und den Rücklauf. Von der Wärmepumpe kommend wird der Vorlauf, je nach Stellung eines 3-Wege-Ventils, entweder durch den Wärmetauscher des Warmwasserspeichers oder durch die Fußbodenheizungen der einzelnen Räume geleitet. Da laut Energiesparverordnung eine Einzelraumregelung vorgeschrieben ist, gibt es an jedem Raum auch einen Stellantrieb (Ventil), das anhand von Raumthermostaaten gesteuert wird. 

{{< figure src="../assets/wärmepumpe.drawio.svg" caption="" attr="" attrlink="" >}}

### Vorlauf, Rücklauf & Heizkurve

Die Umwälzpumpe pumpt Wasser durch die Heizrohre. Das Wasser, das von der Wärmepumpe (wo das Wasser aufgeheizt wird) zu den einzelnen Heizkörpern (Wärmetauscher im Brauchwasser oder Rohre der Fußbodenheizung in den Räumen) nennt sich **Vorlauf**. Während es durch die Heizkörper fließt, kann es dort seine Wärme abgeben und hinter den Heizkörpern im **Rücklauf** zurück zur Wärmepumpe fließen, wo es erneut aufgeheizt werden kann.

Damit die Wärmepumpe weiß ob/wann sie den Vorlauf heizen muss oder nicht, wird fortlaufend die Temperatur des Rücklaufs gemessen, auch wenn die Wärmepumpe gerade nicht heizt. Sinkt die Temperatur des Rücklaufs unter einen bestimmten Wert, der sich aus der [**Heizkurve**](#heizkurve) ergibt, springt der Verdichter der Wärmepumpe an und erhitzt den Vorlauf. Steigt infolgedessen die Rücklauftemperatur über einen weiteren bestimmten Wert, der ebenfalls aus der Heizkurve ergibt, schaltet der Verdichter wieder ab. 

### Warmwasserbereitung

Selbiges passiert auch bei der Warmwasserbereitung, allerdings mit deutlich höheren Temperaturen und nicht anhand der Heizkurve und Rücklauftemperatur, sondern anhand der Warmwasser-Solltemperatur und der fortlaufend gemessenen Temperatur des Warmwassers im Speicher. Zur Warmwasserbereitung wird dadurch mittels des 3 Wege Ventils der Vorlauf nicht durch die Heizrohre der Fußbodenheizung, sondern durch den Wärmetauscher des Warmwasserspeichers geleitet.

### Raumthermostate

Je nach Raumtemperatur schließen/öffnen die Raumthermostate die Rücklaufventile der Rohrleitungen der Fußbodenheizung in den jeweiligen Räumen. Sprich bei geschlossenem Ventil kann der warme Vorlauf von der Wärmepumpe nicht durch den jeweiligen Raum fließen und der Raum wird folglich nicht geheizt.

### Heizkurve

Die Heizkurve, bzw die Kennlinie ist bei vielen Wärmepumpen *Rücklaufgeführt*. Das Bedeutet die Kennlinie gibt anhand ihrer einstellbaren Parameter und der aktellen Außentemperatur einen Sollwert für die Rücklauftemperatur vor. Die einstellbaren Parameter sind üblicherweise:

* Endpunkt (bei -20°C): Bestimmt den Sollwert für den Rücklauf bei -20°C
* Paralleleverschiebung (bei 20°C): TBD...