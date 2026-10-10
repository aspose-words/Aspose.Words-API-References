---
title: "AxisTickLabelPosition"
linktitle: "AxisTickLabelPosition"
second_title: "Aspose.Words para Java"
description: "Especifica las posiciones posibles para las etiquetas de marcas en Java."
type: docs
weight: 30
url: /es/java/com.aspose.words/axisticklabelposition/
---

**Inheritance:**
java.lang.Object
```
public class AxisTickLabelPosition
```

Especifica las posibles posiciones para las etiquetas de marcas.

 **Examples:** 

Muestra cómo insertar un gráfico con valores de fecha/hora.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [DEFAULT](#DEFAULT) | Especifica el valor predeterminado de la posición de las etiquetas de marcas. |
| [HIGH](#HIGH) | Especifica que las etiquetas del eje deben estar en el extremo superior del eje perpendicular. |
| [LOW](#LOW) | Especifica que las etiquetas del eje deben estar en el extremo inferior del eje perpendicular. |
| [NEXT_TO_AXIS](#NEXT-TO-AXIS) | Especifica que las etiquetas del eje deben estar junto al eje. |
| [NONE](#NONE) | Especifica que las etiquetas del eje no se dibujan. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String axisTickLabelPositionName)](#fromName-java.lang.String) |  |
| [getName(int axisTickLabelPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisTickLabelPosition)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Especifica el valor predeterminado de la posición de las etiquetas de marcas.

### HIGH {#HIGH}
```
public static int HIGH
```


Especifica que las etiquetas del eje deben estar en el extremo superior del eje perpendicular.

### LOW {#LOW}
```
public static int LOW
```


Especifica que las etiquetas del eje deben estar en el extremo inferior del eje perpendicular.

### NEXT_TO_AXIS {#NEXT-TO-AXIS}
```
public static int NEXT_TO_AXIS
```


Especifica que las etiquetas del eje deben estar junto al eje.

### NONE {#NONE}
```
public static int NONE
```


Especifica que las etiquetas del eje no se dibujan.

### length {#length}
```
public static int length
```


### fromName(String axisTickLabelPositionName) {#fromName-java.lang.String}
```
public static int fromName(String axisTickLabelPositionName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| axisTickLabelPositionName | java.lang.String |  |

**Returns:**
int
### getName(int axisTickLabelPosition) {#getName-int}
```
public static String getName(int axisTickLabelPosition)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| axisTickLabelPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int axisTickLabelPosition) {#toString-int}
```
public static String toString(int axisTickLabelPosition)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| axisTickLabelPosition | int |  |

**Returns:**
java.lang.String
