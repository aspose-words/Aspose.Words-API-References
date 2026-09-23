---
title: "BubbleSizeCollection"
linktitle: "BubbleSizeCollection"
second_title: "Aspose.Words für Java"
description: "Stellt eine Sammlung von Blasengrößen für eine Diagrammreihe in Java dar."
type: docs
weight: 50
url: /de/java/com.aspose.words/bubblesizecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BubbleSizeCollection implements Iterable
```

Stellt eine Sammlung von Blasengrößen für eine Diagrammreihe dar.

 **Remarks:** 

Die Sammlung erlaubt nur das Ändern von Blasengrößen. Um neue Werte zu einer Diagrammreihe hinzuzufügen oder einzufügen oder Werte zu entfernen, können die entsprechenden Methoden der Klasse [ChartSeries](../../com.aspose.words/chartseries/) verwendet werden.

Leere Blasengrößenwerte werden als double#NA_N.NA_N dargestellt.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get(int index)](#get-int) | Liefert den Blasengrößenwert am angegebenen Index. |
| [getCount()](#getCount) | Liefert die Anzahl der Elemente in dieser Sammlung. |
| [getFormatCode()](#getFormatCode) | Liefert den auf die Blasengrößen angewendeten Formatcode. |
| [iterator()](#iterator) | Gibt ein Enumerator‑Objekt zurück. |
| [set(int index, double value)](#set-int-double) | Setzt den Blasengrößenwert am angegebenen Index. |
| [setFormatCode(String value)](#setFormatCode-java.lang.String) | Setzt den auf die Blasengrößen angewendeten Formatcode. |
### get(int index) {#get-int}
```
public double get(int index)
```


Liefert den Blasengrößenwert am angegebenen Index.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |

**Returns:**
double - Der Blasengrößenwert am angegebenen Index.
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


Liefert den auf die Blasengrößen angewendeten Formatcode.

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
java.lang.String - Der auf die Blasengrößen angewendete Formatcode.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gibt ein Enumerator‑Objekt zurück.

**Returns:**
java.util.Iterator
### set(int index, double value) {#set-int-double}
```
public void set(int index, double value)
```


Setzt den Blasengrößenwert am angegebenen Index.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |
| Wert | double | Der Blasengrößenwert am angegebenen Index. |

### setFormatCode(String value) {#setFormatCode-java.lang.String}
```
public void setFormatCode(String value)
```


Setzt den auf die Blasengrößen angewendeten Formatcode.

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
| Wert | java.lang.String | Der auf die Blasengrößen angewendete Formatcode. |

