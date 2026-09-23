---
title: "ChartSeriesGroupCollection"
linktitle: "ChartSeriesGroupCollection"
second_title: "Aspose.Words für Java"
description: "Stellt eine Sammlung von ChartSeriesGroup‑Objekten in Java dar."
type: docs
weight: 88
url: /de/java/com.aspose.words/chartseriesgroupcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartSeriesGroupCollection implements Iterable
```

Stellt eine Sammlung von [ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/)‑Objekten dar.

 **Remarks:** 

Weitere Informationen finden Sie im Dokumentationsartikel zu [ Working with Charts ][Working with Charts].

 **Examples:** 

Zeigt, wie man mit der sekundären Achse eines Diagramms arbeitet.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(int seriesType)](#add-int) |  |
| [get(int index)](#get-int) | Gibt ein [ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/) am angegebenen Index zurück. |
| [getCount()](#getCount) | Gibt die Anzahl der Seriengruppen in dieser Sammlung zurück. |
| [iterator()](#iterator) | Gibt ein Enumerator‑Objekt zurück. |
| [removeAt(int index)](#removeAt-int) | Entfernt eine Seriengruppe am angegebenen Index. |
### add(int seriesType) {#add-int}
```
public ChartSeriesGroup add(int seriesType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| seriesType | int |  |

**Returns:**
[ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/)
### get(int index) {#get-int}
```
public ChartSeriesGroup get(int index)
```


Gibt ein [ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/) am angegebenen Index zurück.

 **Examples:** 

Zeigt, wie man die sekundäre Achse entfernt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |

**Returns:**
[ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/) - A [ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/) at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Gibt die Anzahl der Seriengruppen in dieser Sammlung zurück.

 **Examples:** 

Zeigt, wie man die sekundäre Achse entfernt.

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
int - Die Anzahl der Seriengruppen in dieser Sammlung.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt ein Enumerator‑Objekt zurück.

**Returns:**
java.util.Iterator
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Entfernt eine Seriengruppe am angegebenen Index. Alle untergeordneten Serien werden aus dem Diagramm entfernt.

 **Examples:** 

Zeigt, wie man die sekundäre Achse entfernt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |

