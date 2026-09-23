---
title: "ChartAxisCollection"
linktitle: "ChartAxisCollection"
second_title: "Aspose.Words für Java"
description: "Stellt eine Sammlung von Diagrammachsen in Java dar."
type: docs
weight: 68
url: /de/java/com.aspose.words/chartaxiscollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartAxisCollection implements Iterable
```

Stellt eine Sammlung von Diagrammachsen dar.

 **Examples:** 

Zeigt, wie mit einer Achsensammlung gearbeitet wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Hide the major grid lines on the primary and secondary Y axes.
 for (ChartAxis axis : chart.getAxes())
 {
     if (axis.getType() == ChartAxisType.VALUE)
         axis.hasMajorGridlines(false);
 }

 doc.save(getArtifactsDir() + "Charts.AxisCollection.docx");
 
```
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get(int index)](#get-int) | Ermittelt die Achse am angegebenen Index. |
| [getCount()](#getCount) | Ermittelt die Anzahl der Achsen in dieser Sammlung. |
| [iterator()](#iterator) | Gibt ein Enumerator‑Objekt zurück. |
### get(int index) {#get-int}
```
public ChartAxis get(int index)
```


Ermittelt die Achse am angegebenen Index.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |

**Returns:**
[ChartAxis](../../com.aspose.words/chartaxis/) - The axis at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Ermittelt die Anzahl der Achsen in dieser Sammlung.

**Returns:**
int - Die Anzahl der Achsen in dieser Sammlung.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt ein Enumerator‑Objekt zurück.

**Returns:**
java.util.Iterator
