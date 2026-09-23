---
title: "ChartAxisCollection"
linktitle: "ChartAxisCollection"
second_title: "Aspose.Words для Java"
description: "Представляет коллекцию осей диаграммы в Java."
type: docs
weight: 68
url: /ru/java/com.aspose.words/chartaxiscollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartAxisCollection implements Iterable
```

Представляет коллекцию осей диаграммы.

 **Examples:** 

Показывает, как работать с коллекцией осей.

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
## Методы

| Метод | Описание |
| --- | --- |
| [get(int index)](#get-int) | Получает ось по указанному индексу. |
| [getCount()](#getCount) | Получает количество осей в этой коллекции. |
| [iterator()](#iterator) | Возвращает объект перечислителя. |
### get(int index) {#get-int}
```
public ChartAxis get(int index)
```


Получает ось по указанному индексу.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int |  |

**Returns:**
[ChartAxis](../../com.aspose.words/chartaxis/) - The axis at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Получает количество осей в этой коллекции.

**Returns:**
int — количество осей в этой коллекции.
### iterator() {#iterator}
```
public Iterator iterator()
```


Возвращает объект перечислителя.

**Returns:**
java.util.Iterator
