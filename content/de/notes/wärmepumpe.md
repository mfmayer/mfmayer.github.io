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

{{< figure src="assets/wärmepumpe.drawio.svg" caption="Bild 1" attr="" attrlink="" >}}

### Vorlauf, Rücklauf

Die Umwälzpumpe pumpt Wasser durch die Heizrohre. Das Wasser, das von der Wärmepumpe (wo das Wasser aufgeheizt wird) zu den einzelnen Heizkörpern (Wärmetauscher im Brauchwasser oder Rohre der Fußbodenheizung in den Räumen) nennt sich **Vorlauf**. Während es durch die Heizkörper fließt, kann es dort seine Wärme abgeben und hinter den Heizkörpern im **Rücklauf** zurück zur Wärmepumpe fließen, wo es erneut aufgeheizt werden kann. Die resultierende Temperaturdifferenz zwischen Vor-/Rücklauf nennt sich **Spreizung**.

### Heizkurve

Damit die Wärmepumpe weiß ob/wann sie den Vorlauf heizen muss oder nicht, wird anhand einer Heizkurve und abhängig von der aktuellen Außentemperatur, ein Sollwert für den Vor- oder Rücklauf (vorlauf-, rücklaufgeführt) festgelegt. Falls es sich wie bei der WPL 6IK um eine nicht um eine modulierende Wärmepumpe handelt (modulierende Wärmepumpen können ihre Heizleistung dynamisch anpassen, um eine gewisse Solltemperatur zu halten), heizt die Wärmepumpe anhand einer Hysterese um die Solltemperatur. Das bedeutet, es wird geheizt bis die aktuelle Temperatur z.B. 2°C über der Solltemperatur liegt, dann wird gewartet bis die Temperatur bis 2°C unterhalb der Solltemperatur abgefallen ist, bevor erneut geheizt wird.

Um die Heizkurve einzustellen gibt es bei der WPL6 IK Wärmepumpe die folgenden Parameter:

* **Endpunkt** (bei -20°C): Bestimmt den Sollwert für den Rücklauf bei -20°C
* **Paralleleverschiebung**: 0K bedeutet 20°C Sollwert bei 20°C Außentemperatur

Das folgende Diagramm zeigt einige Beispiele für deren Werte:

{{< figure src="assets/heizkurve.drawio.svg" caption="" attr="" attrlink="" >}}

### Warmwasserbereitung

Die Warmwasserbereitung funktioniert nach ähnlichem Prinzip, nur mit höheren Temperaturen und nicht anhand der Heizkurve und Rücklauftemperatur, sondern anhand der Warmwasser-Solltemperatur und der fortlaufend gemessenen Temperatur des Warmwassers im Speicher. Zur Warmwasserbereitung wird dadurch mittels des 3 Wege Ventils (siehe Bild1) der Vorlauf nicht durch die Heizrohre der Fußbodenheizung, sondern durch den Wärmetauscher des Warmwasserspeichers geleitet.

### Raumthermostate

Je nach Raumtemperatur schließen/öffnen die Raumthermostate die Rücklaufventile der Rohrleitungen der Fußbodenheizung in den jeweiligen Räumen. Sprich bei geschlossenem Ventil kann der warme Vorlauf von der Wärmepumpe nicht durch den jeweiligen Raum fließen und der Raum wird folglich nicht geheizt.

Sollten sämtliche Raumthermostate geschlossen sein, wird lediglich der Pufferspeicher auf Solltemperatur gebracht und der der Vorlauf fließt unmittelbar durch das Überstromventil wieder als Rücklauf zurück. Sollte dies bei nicht modulierenden Wärmepumpen der Fall sein, erreicht damit die Rücklauftemperatur praktisch unmittelbar die Solltemperatur und der Heizzyklus wird sofort wieder gestoppt. 

Ganz ähnlich wenn nur wenige Raumthermostate geöffnet sind, auch dann werden die Räume praktisch einzeln geheizt und die Soll-Rücklauftemperatur wird sehr viel schneller erreicht, wie wenn der Vorlauf alle Räume zeitgleich durchströmen würde.

### Optimierungen

Zugunsten der Langlebigkeit des Verdichters sollte versucht werden, dass die Wärmepumpe möglichst lange Heizzyklen hat und möglichst wenig taktet. Dazu kann es hilfreich sein, sämtliche Raumthermostate permanent zu öffnen oder zu entfernen. Infolgedessen ergibt sich die Temperatur in den Räumen anhand ihrer jeweiligen Vorlauf Durchflussmenge, sowie der Heizkurve.
