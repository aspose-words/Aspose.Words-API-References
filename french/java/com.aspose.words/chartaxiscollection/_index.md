---
title: "ChartAxisCollection"
linktitle: "ChartAxisCollection"
second_title: "Aspose.Words pour Java"
description: "Représente une collection d'axes de graphique en Java."
type: docs
weight: 68
url: /fr/java/com.aspose.words/chartaxiscollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartAxisCollection implements Iterable
```

Représente une collection d'axes de graphique.

 **Examples:** 

Montre comment travailler avec la collection d'axes.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [get(int index)](#get-int) | Obtient l'axe à l'index spécifié. |
| [getCount()](#getCount) | Obtient le nombre d'axes dans cette collection. |
| [iterator()](#iterator) | Renvoie un objet énumérateur. |
### get(int index) {#get-int}
```
public ChartAxis get(int index)
```


Obtient l'axe à l'index spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[ChartAxis](../../com.aspose.words/chartaxis/) - The axis at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre d'axes dans cette collection.

**Returns:**
int - Le nombre d'axes dans cette collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


Renvoie un objet énumérateur.

**Returns:**
java.util.Iterator
