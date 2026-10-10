---
title: "ChartAxisCollection"
linktitle: "ChartAxisCollection"
second_title: "Aspose.Words para Java"
description: "Representa una colección de ejes de gráfico en Java."
type: docs
weight: 68
url: /es/java/com.aspose.words/chartaxiscollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartAxisCollection implements Iterable
```

Representa una colección de ejes del gráfico.

 **Examples:** 

Muestra cómo trabajar con la colección de ejes.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [get(int index)](#get-int) | Obtiene el eje en el índice especificado. |
| [getCount()](#getCount) | Obtiene el número de ejes en esta colección. |
| [iterator()](#iterator) | Devuelve un objeto enumerador. |
### get(int index) {#get-int}
```
public ChartAxis get(int index)
```


Obtiene el eje en el índice especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |

**Returns:**
[ChartAxis](../../com.aspose.words/chartaxis/) - The axis at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de ejes en esta colección.

**Returns:**
int - El número de ejes en esta colección.
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un objeto enumerador.

**Returns:**
java.util.Iterator
