---
title: "AxisCrosses"
linktitle: "AxisCrosses"
second_title: "Aspose.Words per Java"
description: "Specifica i possibili punti di intersezione per un asse in Java."
type: docs
weight: 25
url: /it/java/com.aspose.words/axiscrosses/
---

**Inheritance:**
java.lang.Object
```
public class AxisCrosses
```

Specifica i possibili punti di intersezione per un asse.

 **Examples:** 

Mostra come inserire un grafico e modificare l'aspetto dei suoi assi.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 Assert.assertEquals(doc, xAxis.getDocument());

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);
 yAxis.getTickLabels().setAlignment(ParagraphAlignment.CENTER);
 yAxis.getTickLabels().getFont().setColor(Color.RED);
 yAxis.getTickLabels().setSpacing(1);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [AUTOMATIC](#AUTOMATIC) | L'asse delle categorie si interseca al punto zero dell'asse dei valori (se possibile), o al valore minimo se il minimo è maggiore di zero, o al massimo se il massimo è inferiore a zero. |
| [CUSTOM](#CUSTOM) | Un asse perpendicolare si interseca al valore specificato dell'asse. |
| [MAXIMUM](#MAXIMUM) | Un asse perpendicolare si interseca al valore massimo dell'asse. |
| [MINIMUM](#MINIMUM) | Un asse perpendicolare si interseca al valore minimo dell'asse. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String axisCrossesName)](#fromName-java.lang.String) |  |
| [getName(int axisCrosses)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisCrosses)](#toString-int) |  |
### AUTOMATIC {#AUTOMATIC}
```
public static int AUTOMATIC
```


L'asse delle categorie si interseca al punto zero dell'asse dei valori (se possibile), o al valore minimo se il minimo è maggiore di zero, o al massimo se il massimo è inferiore a zero.

### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Un asse perpendicolare si interseca al valore specificato dell'asse.

### MAXIMUM {#MAXIMUM}
```
public static int MAXIMUM
```


Un asse perpendicolare si interseca al valore massimo dell'asse.

### MINIMUM {#MINIMUM}
```
public static int MINIMUM
```


Un asse perpendicolare si interseca al valore minimo dell'asse.

### length {#length}
```
public static int length
```


### fromName(String axisCrossesName) {#fromName-java.lang.String}
```
public static int fromName(String axisCrossesName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| axisCrossesName | java.lang.String |  |

**Returns:**
int
### getName(int axisCrosses) {#getName-int}
```
public static String getName(int axisCrosses)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| axisCrosses | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int axisCrosses) {#toString-int}
```
public static String toString(int axisCrosses)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| axisCrosses | int |  |

**Returns:**
java.lang.String
