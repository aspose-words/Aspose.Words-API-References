---
title: "ChartYValueCollection"
linktitle: "ChartYValueCollection"
second_title: "Aspose.Words für Java"
description: "Stellt eine Sammlung von Y-Werten für eine Diagrammreihe in Java dar."
type: docs
weight: 98
url: /de/java/com.aspose.words/chartyvaluecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartYValueCollection implements Iterable
```

Stellt eine Sammlung von Y-Werten für eine Diagrammserie dar.

 **Remarks:** 

Alle Elemente der Sammlung, außer **null**, müssen denselben [ChartYValue.getValueType()](../../com.aspose.words/chartyvalue/\\#getValueType) haben.

Die Sammlung erlaubt nur das Ändern von Y-Werten. Um neue Werte zu einer Diagrammreihe hinzuzufügen oder einzufügen oder Werte zu entfernen, können die entsprechenden Methoden der Klasse [ChartSeries](../../com.aspose.words/chartseries/) verwendet werden.

 **Examples:** 

Zeigt, wie man Diagrammreihendaten abruft.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder();

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series = chart.getSeries().get(0);

 double minValue = Double.MAX_VALUE;
 int minValueIndex = 0;
 double maxValue = -Double.MAX_VALUE;
 int maxValueIndex = 0;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     // Clear individual format of all data points.
     // Data points and data values are one-to-one in column charts.
     series.getDataPoints().get(i).clearFormat();

     // Get Y value.
     double yValue = series.getYValues().get(i).getDoubleValue();

     if (yValue < minValue)
     {
         minValue = yValue;
         minValueIndex = i;
     }

     if (yValue > maxValue)
     {
         maxValue = yValue;
         maxValueIndex = i;
     }
 }

 // Change colors of the max and min values.
 series.getDataPoints().get(minValueIndex).getFormat().getFill().setForeColor(Color.RED);
 series.getDataPoints().get(maxValueIndex).getFormat().getFill().setForeColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Charts.GetChartSeriesData.docx");
 
```
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get(int index)](#get-int) | Liefert den Y-Wert am angegebenen Index. |
| [getCount()](#getCount) | Liefert die Anzahl der Elemente in dieser Sammlung. |
| [getFormatCode()](#getFormatCode) | Liefert den Formatcode, der auf die Y-Werte angewendet wird. |
| [iterator()](#iterator) | Gibt ein Enumerator‑Objekt zurück. |
| [set(int index, ChartYValue value)](#set-int-com.aspose.words.ChartYValue) | Setzt den Y-Wert am angegebenen Index. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | Setzt den Formatcode, der auf die Y-Werte angewendet wird. |
### get(int index) {#get-int}
```
public ChartYValue get(int index)
```


Liefert den Y-Wert am angegebenen Index.

 **Remarks:** 

Leere Werte werden als **null** dargestellt.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/) - The Y value at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Liefert die Anzahl der Elemente in dieser Sammlung.

**Returns:**
int - Die Anzahl der Elemente in dieser Sammlung.
### getFormatCode() {#getFormatCode}
```
public String getFormatCode()
```


Liefert den Formatcode, der auf die Y-Werte angewendet wird.

 **Remarks:** 

Die Zahlenformatierung wird verwendet, um die Darstellung der Werte im Diagramm zu ändern. Beispiele für Zahlenformate:

Zahl - "\\#,\\#\\#0.00"

Währung - "\\"$\\"\#,\#\#0.00"

Zeit - "[$-x-systime]h:mm:ss AM/PM"

Datum - "d/mm/yyyy"

Prozent - "0.00%"

Bruch - "\# ?/?"

Wissenschaftlich - "0.00E+00"

Buchhaltung - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Benutzerdefiniert mit Farbe - "[Red]-\#,\#\#0.0"

 **Examples:** 

Zeigt, wie man mit dem Formatcode der Diagrammdaten arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Bubble chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 ChartSeries series = chart.getSeries().add(
         "Series1",
         new double[] { 1.0, 1.9, 2.45, 3.0 },
         new double[] { 1.0, -0.9, 1.82, 0.0 },
         new double[] { 2.0, 1.1, 2.95, 2.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowCategoryName(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowBubbleSize(true);

 // Set data format codes.
 series.getXValues().setFormatCode("#,##0.0#");
 series.getYValues().setFormatCode("#,##0.0#;[Red]\\-#,##0.0#");
 series.getBubbleSizes().setFormatCode("#,##0.0#");

 doc.save(getArtifactsDir() + "Charts.FormatCode.docx");
 
```

**Returns:**
java.lang.String - Der Formatcode, der auf die Y‑Werte angewendet wird.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt ein Enumerator‑Objekt zurück.

**Returns:**
java.util.Iterator
### set(int index, ChartYValue value) {#set-int-com.aspose.words.ChartYValue}
```
public void set(int index, ChartYValue value)
```


Setzt den Y-Wert am angegebenen Index.

 **Remarks:** 

Leere Werte werden als **null** dargestellt.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |
| value | [ChartYValue](../../com.aspose.words/chartyvalue/) | Der Y‑Wert am angegebenen Index. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


Setzt den Formatcode, der auf die Y-Werte angewendet wird.

 **Remarks:** 

Die Zahlenformatierung wird verwendet, um die Darstellung der Werte im Diagramm zu ändern. Beispiele für Zahlenformate:

Zahl - "\\#,\\#\\#0.00"

Währung - "\\"$\\"\#,\#\#0.00"

Zeit - "[$-x-systime]h:mm:ss AM/PM"

Datum - "d/mm/yyyy"

Prozent - "0.00%"

Bruch - "\# ?/?"

Wissenschaftlich - "0.00E+00"

Buchhaltung - "\_-\\"$\\"\* \#,\#\#0.00\_-;-\\"$\\"\* \#,\#\#0.00\_-;\_-\\"$\\"\* \\"-\\"??\_-;\_-@\_-"

Benutzerdefiniert mit Farbe - "[Red]-\#,\#\#0.0"

 **Examples:** 

Zeigt, wie man mit dem Formatcode der Diagrammdaten arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Bubble chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 ChartSeries series = chart.getSeries().add(
         "Series1",
         new double[] { 1.0, 1.9, 2.45, 3.0 },
         new double[] { 1.0, -0.9, 1.82, 0.0 },
         new double[] { 2.0, 1.1, 2.95, 2.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowCategoryName(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowBubbleSize(true);

 // Set data format codes.
 series.getXValues().setFormatCode("#,##0.0#");
 series.getYValues().setFormatCode("#,##0.0#;[Red]\\-#,##0.0#");
 series.getBubbleSizes().setFormatCode("#,##0.0#");

 doc.save(getArtifactsDir() + "Charts.FormatCode.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Formatcode, der auf die Y‑Werte angewendet wird. |

