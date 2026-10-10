---
title: "AxisTickMark"
linktitle: "AxisTickMark"
second_title: "Aspose.Words per Java"
description: "Specifica le possibili posizioni per i segni di graduazione in Java."
type: docs
weight: 32
url: /it/java/com.aspose.words/axistickmark/
---

**Inheritance:**
java.lang.Object
```
public class AxisTickMark
```

Specifica le possibili posizioni per i segni di tic.

 **Examples:** 

Mostra come inserire un grafico con valori data/ora.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [CROSS](#CROSS) | Specifica che i segni di graduazione devono attraversare l'asse. |
| [INSIDE](#INSIDE) | Specifica che i segni di graduazione devono trovarsi all'interno dell'area del grafico. |
| [NONE](#NONE) | Specifica che non ci devono essere segni di graduazione. |
| [OUTSIDE](#OUTSIDE) | Specifica che i segni di graduazione devono trovarsi al di fuori dell'area del grafico. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String axisTickMarkName)](#fromName-java.lang.String) |  |
| [getName(int axisTickMark)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisTickMark)](#toString-int) |  |
### CROSS {#CROSS}
```
public static int CROSS
```


Specifica che i segni di graduazione devono attraversare l'asse.

### INSIDE {#INSIDE}
```
public static int INSIDE
```


Specifica che i segni di graduazione devono trovarsi all'interno dell'area del grafico.

### NONE {#NONE}
```
public static int NONE
```


Specifica che non ci devono essere segni di graduazione.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


Specifica che i segni di graduazione devono trovarsi al di fuori dell'area del grafico.

### length {#length}
```
public static int length
```


### fromName(String axisTickMarkName) {#fromName-java.lang.String}
```
public static int fromName(String axisTickMarkName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| axisTickMarkName | java.lang.String |  |

**Returns:**
int
### getName(int axisTickMark) {#getName-int}
```
public static String getName(int axisTickMark)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| axisTickMark | int |  |

**Returns:**
java.lang.String
