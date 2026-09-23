---
title: "ChartLegendEntry"
linktitle: "ChartLegendEntry"
second_title: "Aspose.Words für Java"
description: "Stellt einen Eintrag der Diagrammlegende in Java dar."
type: docs
weight: 80
url: /de/java/com.aspose.words/chartlegendentry/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartLegendEntry implements Cloneable
```

Stellt einen Eintrag der Diagrammlegende dar.

Weitere Informationen finden Sie im Dokumentationsartikel zu [ Working with Charts ][Working with Charts].

 **Remarks:** 

Ein Legendeeintrag entspricht einer bestimmten Diagrammreihe oder Trendlinie.

Der Text des Eintrags ist der Name der Reihe oder Trendlinie. Der Text kann nicht geändert werden.

 **Examples:** 

Zeigt, wie man mit einer Legenden‑Schriftart arbeitet.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Chart series (Java).docx");
 Chart chart = ((Shape)doc.getChild(NodeType.SHAPE, 0, true)).getChart();

 ChartLegend chartLegend = chart.getLegend();
 // Set default font size all legend entries.
 chartLegend.getFont().setSize(14.0);
 // Change font for specific legend entry.
 chartLegend.getLegendEntries().get(1).getFont().setItalic(true);
 chartLegend.getLegendEntries().get(1).getFont().setSize(12.0);
 // Get legend entry for chart series.
 ChartLegendEntry legendEntry = chart.getSeries().get(0).getLegendEntry();

 doc.save(getArtifactsDir() + "Charts.LegendFont.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fetchSpecialDefaultRunPropertyValue(int key)](#fetchSpecialDefaultRunPropertyValue-int) |  |
| [generateItemText()](#generateItemText) |  |
| [getFont()](#getFont) | Bietet Zugriff auf die Schriftformatierung dieses Legendeeintrags. |
| [getRelativePropertyValue(int key, Object value)](#getRelativePropertyValue-int-java.lang.Object) |  |
| [isHidden()](#isHidden) | Ruft einen Wert ab, der angibt, ob dieser Eintrag in der Diagrammlegende ausgeblendet ist. |
| [isHidden(boolean value)](#isHidden-boolean) | Legt einen Wert fest, der angibt, ob dieser Eintrag in der Diagrammlegende ausgeblendet ist. |
### fetchSpecialDefaultRunPropertyValue(int key) {#fetchSpecialDefaultRunPropertyValue-int}
```
public Object fetchSpecialDefaultRunPropertyValue(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### generateItemText() {#generateItemText}
```
public String generateItemText()
```




**Returns:**
java.lang.String
### getFont() {#getFont}
```
public Font getFont()
```


Bietet Zugriff auf die Schriftformatierung dieses Legendeeintrags.

 **Examples:** 

Zeigt, wie man mit einer Legenden‑Schriftart arbeitet.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Chart series (Java).docx");
 Chart chart = ((Shape)doc.getChild(NodeType.SHAPE, 0, true)).getChart();

 ChartLegend chartLegend = chart.getLegend();
 // Set default font size all legend entries.
 chartLegend.getFont().setSize(14.0);
 // Change font for specific legend entry.
 chartLegend.getLegendEntries().get(1).getFont().setItalic(true);
 chartLegend.getLegendEntries().get(1).getFont().setSize(12.0);
 // Get legend entry for chart series.
 ChartLegendEntry legendEntry = chart.getSeries().get(0).getLegendEntry();

 doc.save(getArtifactsDir() + "Charts.LegendFont.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getRelativePropertyValue(int key, Object value) {#getRelativePropertyValue-int-java.lang.Object}
```
public Object getRelativePropertyValue(int key, Object value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| Wert | java.lang.Object |  |

**Returns:**
java.lang.Object
### isHidden() {#isHidden}
```
public boolean isHidden()
```


Ruft einen Wert ab, der angibt, ob dieser Eintrag in der Diagrammlegende ausgeblendet ist. Der Standardwert ist **false**.

 **Remarks:** 

Wenn ein Diagrammlegendeeintrag ausgeblendet ist, wirkt sich das nicht auf die entsprechende Diagrammreihe oder Trendlinie aus, die weiterhin im Diagramm angezeigt wird.

 **Examples:** 

Zeigt, wie man mit einem Legenden-Eintrag für Diagrammserien arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();
 series.clear();

 String[] categories = new String[] { "AW Category 1", "AW Category 2" };

 ChartSeries series1 = series.add("Series 1", categories, new double[] { 1.0, 2.0 });
 series.add("Series 2", categories, new double[] { 3.0, 4.0 });
 series.add("Series 3", categories, new double[] { 5.0, 6.0 });
 series.add("Series 4", categories, new double[] { 0.0, 0.0 });

 ChartLegendEntryCollection legendEntries = chart.getLegend().getLegendEntries();
 legendEntries.get(3).isHidden(true);

 doc.save(getArtifactsDir() + "Charts.LegendEntries.docx");
 
```

**Returns:**
boolean - Ein Wert, der angibt, ob dieser Eintrag in der Diagrammlegende ausgeblendet ist.
### isHidden(boolean value) {#isHidden-boolean}
```
public void isHidden(boolean value)
```


Legt einen Wert fest, der angibt, ob dieser Eintrag in der Diagrammlegende ausgeblendet ist. Der Standardwert ist **false**.

 **Remarks:** 

Wenn ein Diagrammlegendeeintrag ausgeblendet ist, wirkt sich das nicht auf die entsprechende Diagrammreihe oder Trendlinie aus, die weiterhin im Diagramm angezeigt wird.

 **Examples:** 

Zeigt, wie man mit einem Legenden-Eintrag für Diagrammserien arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();
 series.clear();

 String[] categories = new String[] { "AW Category 1", "AW Category 2" };

 ChartSeries series1 = series.add("Series 1", categories, new double[] { 1.0, 2.0 });
 series.add("Series 2", categories, new double[] { 3.0, 4.0 });
 series.add("Series 3", categories, new double[] { 5.0, 6.0 });
 series.add("Series 4", categories, new double[] { 0.0, 0.0 });

 ChartLegendEntryCollection legendEntries = chart.getLegend().getLegendEntries();
 legendEntries.get(3).isHidden(true);

 doc.save(getArtifactsDir() + "Charts.LegendEntries.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Wert, der angibt, ob dieser Eintrag in der Diagrammlegende ausgeblendet ist. |

