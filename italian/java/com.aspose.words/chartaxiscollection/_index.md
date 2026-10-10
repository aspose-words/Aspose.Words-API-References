---
title: "ChartAxisCollection"
linktitle: "ChartAxisCollection"
second_title: "Aspose.Words per Java"
description: "Rappresenta una raccolta di assi del grafico in Java."
type: docs
weight: 68
url: /it/java/com.aspose.words/chartaxiscollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartAxisCollection implements Iterable
```

Rappresenta una raccolta di assi del grafico.

 **Examples:** 

Mostra come lavorare con la raccolta di assi.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get(int index)](#get-int) | Ottiene l'asse all'indice specificato. |
| [getCount()](#getCount) | Ottiene il numero di assi in questa raccolta. |
| [iterator()](#iterator) | Restituisce un oggetto enumeratore. |
### get(int index) {#get-int}
```
public ChartAxis get(int index)
```


Ottiene l'asse all'indice specificato.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |

**Returns:**
[ChartAxis](../../com.aspose.words/chartaxis/) - The axis at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Ottiene il numero di assi in questa raccolta.

**Returns:**
int - Il numero di assi in questa raccolta.
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un oggetto enumeratore.

**Returns:**
java.util.Iterator
