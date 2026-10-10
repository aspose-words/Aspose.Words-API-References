---
title: "ChartSeriesGroupCollection"
linktitle: "ChartSeriesGroupCollection"
second_title: "Aspose.Words для Java"
description: "Представляет коллекцию объектов ChartSeriesGroup в Java."
type: docs
weight: 88
url: /ru/java/com.aspose.words/chartseriesgroupcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartSeriesGroupCollection implements Iterable
```

Представляет коллекцию объектов [ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/).

 **Remarks:** 

Чтобы узнать больше, посетите статью документации [ Working with Charts ][Working with Charts].

 **Examples:** 

Показывает, как работать со вторичной осью диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Методы

| Метод | Описание |
| --- | --- |
| [add(int seriesType)](#add-int) |  |
| [get(int index)](#get-int) | Возвращает [ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/) по указанному индексу. |
| [getCount()](#getCount) | Возвращает количество групп серий в этой коллекции. |
| [iterator()](#iterator) | Возвращает объект перечислителя. |
| [removeAt(int index)](#removeAt-int) | Удаляет группу серий по указанному индексу. |
### add(int seriesType) {#add-int}
```
public ChartSeriesGroup add(int seriesType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| seriesType | int |  |

**Returns:**
[ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/)
### get(int index) {#get-int}
```
public ChartSeriesGroup get(int index)
```


Возвращает [ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/) по указанному индексу.

 **Examples:** 

Показывает, как удалить вторичную ось.

```

 Document doc = new Document(getMyDir() + "Combo chart.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Chart chart = shape.getChart();
 ChartSeriesGroupCollection seriesGroups = chart.getSeriesGroups();

 // Find secondary axis and remove from the collection.
 for (int i = 0; i < seriesGroups.getCount(); i++)
     if (seriesGroups.get(i).getAxisGroup() == AxisGroup.SECONDARY)
         seriesGroups.removeAt(i);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int |  |

**Returns:**
[ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/) - A [ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/) at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Возвращает количество групп серий в этой коллекции.

 **Examples:** 

Показывает, как удалить вторичную ось.

```

 Document doc = new Document(getMyDir() + "Combo chart.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Chart chart = shape.getChart();
 ChartSeriesGroupCollection seriesGroups = chart.getSeriesGroups();

 // Find secondary axis and remove from the collection.
 for (int i = 0; i < seriesGroups.getCount(); i++)
     if (seriesGroups.get(i).getAxisGroup() == AxisGroup.SECONDARY)
         seriesGroups.removeAt(i);
 
```

**Returns:**
int - Количество групп серий в этой коллекции.
### iterator() {#iterator}
```
public Iterator iterator()
```


Возвращает объект перечислителя.

**Returns:**
java.util.Iterator
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Удаляет группу серий по указанному индексу. Все дочерние серии будут удалены из диаграммы.

 **Examples:** 

Показывает, как удалить вторичную ось.

```

 Document doc = new Document(getMyDir() + "Combo chart.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Chart chart = shape.getChart();
 ChartSeriesGroupCollection seriesGroups = chart.getSeriesGroups();

 // Find secondary axis and remove from the collection.
 for (int i = 0; i < seriesGroups.getCount(); i++)
     if (seriesGroups.get(i).getAxisGroup() == AxisGroup.SECONDARY)
         seriesGroups.removeAt(i);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int |  |

