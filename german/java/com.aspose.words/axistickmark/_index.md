---
title: "AxisTickMark"
linktitle: "AxisTickMark"
second_title: "Aspose.Words für Java"
description: "Gibt die möglichen Positionen für Tick-Marken in Java an."
type: docs
weight: 32
url: /de/java/com.aspose.words/axistickmark/
---

**Inheritance:**
java.lang.Object
```
public class AxisTickMark
```

Gibt die möglichen Positionen für Achsenmarkierungen an.

 **Examples:** 

Zeigt, wie man ein Diagramm mit Datum/Zeit-Werten einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 Date datetimeMin = DocumentHelper.createDate(2017, 11, 5);
 xAxis.getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(2017, 12, 3);
 xAxis.getScaling().setMaximum(new AxisBound(datetimeMax));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CROSS](#CROSS) | Gibt an, dass die Tick-Marken die Achse kreuzen sollen. |
| [INSIDE](#INSIDE) | Gibt an, dass die Teilstriche innerhalb des Diagrammbereichs liegen sollen. |
| [NONE](#NONE) | Gibt an, dass keine Teilstriche vorhanden sein sollen. |
| [OUTSIDE](#OUTSIDE) | Gibt an, dass die Teilstriche außerhalb des Diagrammbereichs liegen sollen. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String axisTickMarkName)](#fromName-java.lang.String) |  |
| [getName(int axisTickMark)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisTickMark)](#toString-int) |  |
### CROSS {#CROSS}
```
public static int CROSS
```


Gibt an, dass die Tick-Marken die Achse kreuzen sollen.

### INSIDE {#INSIDE}
```
public static int INSIDE
```


Gibt an, dass die Teilstriche innerhalb des Diagrammbereichs liegen sollen.

### NONE {#NONE}
```
public static int NONE
```


Gibt an, dass keine Teilstriche vorhanden sein sollen.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


Gibt an, dass die Teilstriche außerhalb des Diagrammbereichs liegen sollen.

### length {#length}
```
public static int length
```


### fromName(String axisTickMarkName) {#fromName-java.lang.String}
```
public static int fromName(String axisTickMarkName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| axisTickMarkName | java.lang.String |  |

**Returns:**
int
### getName(int axisTickMark) {#getName-int}
```
public static String getName(int axisTickMark)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| axisTickMark | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int axisTickMark) {#toString-int}
```
public static String toString(int axisTickMark)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| axisTickMark | int |  |

**Returns:**
java.lang.String
