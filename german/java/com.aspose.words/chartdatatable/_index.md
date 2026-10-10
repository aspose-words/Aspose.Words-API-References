---
title: "ChartDataTable"
linktitle: "ChartDataTable"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Festlegen von Eigenschaften einer Diagrammdatentabelle in Java."
type: docs
weight: 77
url: /de/java/com.aspose.words/chartdatatable/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartDataTable implements Cloneable
```

Ermöglicht die Angabe von Eigenschaften einer Diagrammdatentabelle.

 **Examples:** 

Zeigt, wie man die Datentabelle mit den Diagrammseriendaten anzeigt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fetchSpecialDefaultRunPropertyValue(int key)](#fetchSpecialDefaultRunPropertyValue-int) |  |
| [generateItemText()](#generateItemText) |  |
| [getFont()](#getFont) | Stellt Zugriff auf die Schriftformatierung der Datentabelle bereit. |
| [getFormat()](#getFormat) | Stellt Zugriff auf die Füllung des Texthintergrunds und die Rahmenformatierung der Datentabelle bereit. |
| [getRelativePropertyValue(int key, Object value)](#getRelativePropertyValue-int-java.lang.Object) |  |
| [getShapeType()](#getShapeType) |  |
| [getShow()](#getShow) | Gibt ein Flag zurück, das angibt, ob die Datentabelle für das Diagramm angezeigt wird. |
| [hasHorizontalBorder()](#hasHorizontalBorder) | Gibt ein Flag zurück, das angibt, ob ein horizontaler Rahmen der Datentabelle angezeigt wird. |
| [hasHorizontalBorder(boolean value)](#hasHorizontalBorder-boolean) | Setzt ein Flag, das angibt, ob ein horizontaler Rahmen der Datentabelle angezeigt wird. |
| [hasLegendKeys()](#hasLegendKeys) | Gibt ein Flag zurück, das angibt, ob Legenden‑Schlüssel in der Datentabelle angezeigt werden. |
| [hasLegendKeys(boolean value)](#hasLegendKeys-boolean) | Setzt ein Flag, das angibt, ob Legenden‑Schlüssel in der Datentabelle angezeigt werden. |
| [hasOutlineBorder()](#hasOutlineBorder) | Gibt ein Flag zurück, das angibt, ob ein Umrissrahmen, d. h. ein Rahmen um Serien‑ und Kategorienamen, angezeigt wird. |
| [hasOutlineBorder(boolean value)](#hasOutlineBorder-boolean) | Setzt ein Flag, das angibt, ob ein Umrissrahmen, d. h. ein Rahmen um Serien‑ und Kategorienamen, angezeigt wird. |
| [hasVerticalBorder()](#hasVerticalBorder) | Gibt ein Flag zurück, das angibt, ob ein vertikaler Rahmen der Datentabelle angezeigt wird. |
| [hasVerticalBorder(boolean value)](#hasVerticalBorder-boolean) | Setzt ein Flag, das angibt, ob ein vertikaler Rahmen der Datentabelle angezeigt wird. |
| [isFillSupported()](#isFillSupported) |  |
| [isFormatDefined()](#isFormatDefined) |  |
| [materializeSpPr()](#materializeSpPr) |  |
| [setShapeType(int value)](#setShapeType-int) |  |
| [setShow(boolean value)](#setShow-boolean) | Setzt ein Flag, das angibt, ob die Datentabelle für das Diagramm angezeigt wird. |
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


Stellt Zugriff auf die Schriftformatierung der Datentabelle bereit.

 **Examples:** 

Zeigt, wie man die Datentabelle mit den Diagrammseriendaten anzeigt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getFormat() {#getFormat}
```
public ChartFormat getFormat()
```


Stellt Zugriff auf die Füllung des Texthintergrunds und die Rahmenformatierung der Datentabelle bereit.

 **Examples:** 

Zeigt, wie man die Datentabelle mit den Diagrammseriendaten anzeigt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Returns:**
[ChartFormat](../../com.aspose.words/chartformat/) - The corresponding [ChartFormat](../../com.aspose.words/chartformat/) value.
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
### getShapeType() {#getShapeType}
```
public int getShapeType()
```




**Returns:**
int
### getShow() {#getShow}
```
public boolean getShow()
```


Gibt ein Flag zurück, das angibt, ob die Datentabelle für das Diagramm angezeigt wird. Der Standardwert ist false.

 **Remarks:** 

Die folgenden Diagrammtypen unterstützen keine Datentabellen: Scatter, Pie, Doughnut, Surface, Radar, Treemap, Sunburst, Histogram, Pareto, Box‑and‑Whisker, Waterfall, Funnel, Kombinationsdiagramme, die Serien dieser Typen enthalten. Das Anzeigen einer Datentabelle für diese Diagrammtypen wirft eine java.lang.IllegalStateException‑Ausnahme.

 **Examples:** 

Zeigt, wie man die Datentabelle mit den Diagrammseriendaten anzeigt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Returns:**
boolean – Ein Flag, das angibt, ob die Datentabelle für das Diagramm angezeigt wird.
### hasHorizontalBorder() {#hasHorizontalBorder}
```
public boolean hasHorizontalBorder()
```


Gibt ein Flag zurück, das angibt, ob ein horizontaler Rahmen der Datentabelle angezeigt wird. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie man die Datentabelle mit den Diagrammseriendaten anzeigt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Returns:**
boolean - Ein Flag, das angibt, ob ein horizontaler Rand der Datentabelle angezeigt wird.
### hasHorizontalBorder(boolean value) {#hasHorizontalBorder-boolean}
```
public void hasHorizontalBorder(boolean value)
```


Setzt ein Flag, das angibt, ob ein horizontaler Rand der Datentabelle angezeigt wird. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie man die Datentabelle mit den Diagrammseriendaten anzeigt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Flag, das angibt, ob ein horizontaler Rand der Datentabelle angezeigt wird. |

### hasLegendKeys() {#hasLegendKeys}
```
public boolean hasLegendKeys()
```


Liest ein Flag, das angibt, ob Legenden‑Schlüssel in der Datentabelle angezeigt werden. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie man die Datentabelle mit den Diagrammseriendaten anzeigt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Returns:**
boolean - Ein Flag, das angibt, ob Legenden‑Schlüssel in der Datentabelle angezeigt werden.
### hasLegendKeys(boolean value) {#hasLegendKeys-boolean}
```
public void hasLegendKeys(boolean value)
```


Setzt ein Flag, das angibt, ob Legenden‑Schlüssel in der Datentabelle angezeigt werden. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie man die Datentabelle mit den Diagrammseriendaten anzeigt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Flag, das angibt, ob Legenden‑Schlüssel in der Datentabelle angezeigt werden. |

### hasOutlineBorder() {#hasOutlineBorder}
```
public boolean hasOutlineBorder()
```


Liest ein Flag, das angibt, ob ein Umrandungsrahmen, d. h. ein Rand um Reihen‑ und Kategorienamen, angezeigt wird. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie man die Datentabelle mit den Diagrammseriendaten anzeigt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Returns:**
boolean - Ein Flag, das angibt, ob ein Umrandungsrahmen, d. h. ein Rand um Reihen‑ und Kategorienamen, angezeigt wird.
### hasOutlineBorder(boolean value) {#hasOutlineBorder-boolean}
```
public void hasOutlineBorder(boolean value)
```


Setzt ein Flag, das angibt, ob ein Umrandungsrahmen, d. h. ein Rand um Reihen‑ und Kategorienamen, angezeigt wird. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie man die Datentabelle mit den Diagrammseriendaten anzeigt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Flag, das angibt, ob ein Umrandungsrahmen, d. h. ein Rand um Reihen‑ und Kategorienamen, angezeigt wird. |

### hasVerticalBorder() {#hasVerticalBorder}
```
public boolean hasVerticalBorder()
```


Liest ein Flag, das angibt, ob ein vertikaler Rand der Datentabelle angezeigt wird. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie man die Datentabelle mit den Diagrammseriendaten anzeigt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Returns:**
boolean - Ein Flag, das angibt, ob ein vertikaler Rand der Datentabelle angezeigt wird.
### hasVerticalBorder(boolean value) {#hasVerticalBorder-boolean}
```
public void hasVerticalBorder(boolean value)
```


Setzt ein Flag, das angibt, ob ein vertikaler Rand der Datentabelle angezeigt wird. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie man die Datentabelle mit den Diagrammseriendaten anzeigt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Flag, das angibt, ob ein vertikaler Rand der Datentabelle angezeigt wird. |

### isFillSupported() {#isFillSupported}
```
public boolean isFillSupported()
```




**Returns:**
boolean
### isFormatDefined() {#isFormatDefined}
```
public boolean isFormatDefined()
```




**Returns:**
boolean
### materializeSpPr() {#materializeSpPr}
```
public void materializeSpPr()
```




### setShapeType(int value) {#setShapeType-int}
```
public void setShapeType(int value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int |  |

### setShow(boolean value) {#setShow-boolean}
```
public void setShow(boolean value)
```


Setzt ein Flag, das angibt, ob die Datentabelle für das Diagramm angezeigt wird. Der Standardwert ist false.

 **Remarks:** 

Die folgenden Diagrammtypen unterstützen keine Datentabellen: Scatter, Pie, Doughnut, Surface, Radar, Treemap, Sunburst, Histogram, Pareto, Box‑and‑Whisker, Waterfall, Funnel, Kombinationsdiagramme, die Serien dieser Typen enthalten. Das Anzeigen einer Datentabelle für diese Diagrammtypen wirft eine java.lang.IllegalStateException‑Ausnahme.

 **Examples:** 

Zeigt, wie man die Datentabelle mit den Diagrammseriendaten anzeigt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Flag, das angibt, ob die Datentabelle für das Diagramm angezeigt wird. |

