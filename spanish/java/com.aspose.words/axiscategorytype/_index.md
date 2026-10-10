---
title: "AxisCategoryType"
linktitle: "AxisCategoryType"
second_title: "Aspose.Words para Java"
description: "Especifica el tipo de un eje de categoría en Java."
type: docs
weight: 24
url: /es/java/com.aspose.words/axiscategorytype/
---

**Inheritance:**
java.lang.Object
```
public class AxisCategoryType
```

Especifica el tipo de un eje de categoría.

 **Examples:** 

Muestra cómo insertar un gráfico y modificar la apariencia de sus ejes.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [AUTOMATIC](#AUTOMATIC) | Especifica que el tipo de un eje de categoría se determina automáticamente en función de los datos. |
| [CATEGORY](#CATEGORY) | Especifica un eje de un conjunto arbitrario de categorías. |
| [TIME](#TIME) | Especifica un eje de categoría de tiempo. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String axisCategoryTypeName)](#fromName-java.lang.String) |  |
| [getName(int axisCategoryType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisCategoryType)](#toString-int) |  |
### AUTOMATIC {#AUTOMATIC}
```
public static int AUTOMATIC
```


Especifica que el tipo de un eje de categoría se determina automáticamente en función de los datos.

### CATEGORY {#CATEGORY}
```
public static int CATEGORY
```


Especifica un eje de un conjunto arbitrario de categorías.

### TIME {#TIME}
```
public static int TIME
```


Especifica un eje de categoría de tiempo.

### length {#length}
```
public static int length
```


### fromName(String axisCategoryTypeName) {#fromName-java.lang.String}
```
public static int fromName(String axisCategoryTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| axisCategoryTypeName | java.lang.String |  |

**Returns:**
int
### getName(int axisCategoryType) {#getName-int}
```
public static String getName(int axisCategoryType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| axisCategoryType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int axisCategoryType) {#toString-int}
```
public static String toString(int axisCategoryType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| axisCategoryType | int |  |

**Returns:**
java.lang.String
