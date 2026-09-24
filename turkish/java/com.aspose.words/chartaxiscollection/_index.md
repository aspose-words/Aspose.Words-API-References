---
title: "ChartAxisCollection"
linktitle: "ChartAxisCollection"
second_title: "Aspose.Words Java için"
description: "Java'da bir grafik eksenleri koleksiyonunu temsil eder."
type: docs
weight: 68
url: /tr/java/com.aspose.words/chartaxiscollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartAxisCollection implements Iterable
```

Grafik eksenlerinin bir koleksiyonunu temsil eder.

 **Examples:** 

Eksen koleksiyonu ile nasıl çalışılacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get(int index)](#get-int) | Belirtilen indeksteki ekseni alır. |
| [getCount()](#getCount) | Bu koleksiyondaki eksen sayısını alır. |
| [iterator()](#iterator) | Bir enumerator nesnesi döndürür. |
### get(int index) {#get-int}
```
public ChartAxis get(int index)
```


Belirtilen indeksteki ekseni alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int |  |

**Returns:**
[ChartAxis](../../com.aspose.words/chartaxis/) - The axis at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Bu koleksiyondaki eksen sayısını alır.

**Returns:**
int - Bu koleksiyondaki eksen sayısı.
### iterator() {#iterator}
```
public Iterator iterator()
```


Bir enumerator nesnesi döndürür.

**Returns:**
java.util.Iterator
