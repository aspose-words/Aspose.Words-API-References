---
title: "AxisBuiltInUnit"
linktitle: "AxisBuiltInUnit"
second_title: "Aspose.Words para Java"
description: "Especifica las unidades de visualización para un eje en Java."
type: docs
weight: 23
url: /es/java/com.aspose.words/axisbuiltinunit/
---

**Inheritance:**
java.lang.Object
```
public class AxisBuiltInUnit
```

Especifica las unidades de visualización para un eje.

 **Examples:** 

Muestra cómo manipular las marcas de graduación y los valores mostrados de un eje de gráfico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());

 // Set the minor tick marks of the Y-axis to point away from the plot area,
 // and the major tick marks to cross the axis.
 ChartAxis axis = chart.getAxisY();
 axis.setMajorTickMark(AxisTickMark.CROSS);
 axis.setMinorTickMark(AxisTickMark.OUTSIDE);

 // Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(1.0);

 // Set the Y-axis bounds to -10 and 20.
 // This Y-axis will now display 4 major tick marks and 27 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(20.0));

 // For the X-axis, set the major tick marks at every 10 units,
 // every minor tick mark at 2.5 units.
 axis = chart.getAxisX();
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(2.5);

 // Configure both types of tick marks to appear inside the graph plot area.
 axis.setMajorTickMark(AxisTickMark.INSIDE);
 axis.setMinorTickMark(AxisTickMark.INSIDE);

 // Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(30.0));
 axis.getTickLabels().setAlignment(ParagraphAlignment.RIGHT);

 Assert.assertEquals(1, axis.getTickLabels().getSpacing());
 Assert.assertEquals(doc, axis.getDisplayUnit().getDocument());

 // Set the tick labels to display their value in millions.
 axis.getDisplayUnit().setUnit(AxisBuiltInUnit.MILLIONS);

 // We can set a more specific value by which tick labels will display their values.
 // This statement is equivalent to the one above.
 axis.getDisplayUnit().setCustomUnit(1000000.0);
 doc.save(getArtifactsDir() + "Charts.AxisDisplayUnit.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [BILLIONS](#BILLIONS) | Especifica que los valores del gráfico se dividirán por 1,000,000,000. |
| [CUSTOM](#CUSTOM) | Especifica que los valores del gráfico se dividirán por un divisor definido por el usuario. |
| [HUNDREDS](#HUNDREDS) | Especifica que los valores del gráfico se dividirán por 100. |
| [HUNDRED_MILLIONS](#HUNDRED-MILLIONS) | Especifica que los valores del gráfico se dividirán por 100,000,000. |
| [HUNDRED_THOUSANDS](#HUNDRED-THOUSANDS) | Especifica que los valores del gráfico se dividirán por 100,000. |
| [MILLIONS](#MILLIONS) | Especifica que los valores del gráfico se dividirán por 1,000,000. |
| [NONE](#NONE) | Especifica que los valores del gráfico se mostrarán tal como están. |
| [PERCENTAGE](#PERCENTAGE) | Especifica que los valores del gráfico se dividirán por 0.01. |
| [TEN_MILLIONS](#TEN-MILLIONS) | Especifica que los valores del gráfico se dividirán por 10,000,000. |
| [TEN_THOUSANDS](#TEN-THOUSANDS) | Especifica que los valores del gráfico se dividirán por 10,000. |
| [THOUSANDS](#THOUSANDS) | Especifica que los valores del gráfico se dividirán por 1,000. |
| [TRILLIONS](#TRILLIONS) | Especifica que los valores del gráfico se dividirán por 1,000,000,000,0000. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String axisBuiltInUnitName)](#fromName-java.lang.String) |  |
| [getName(int axisBuiltInUnit)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisBuiltInUnit)](#toString-int) |  |
### BILLIONS {#BILLIONS}
```
public static int BILLIONS
```


Especifica que los valores del gráfico se dividirán por 1,000,000,000.

### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Especifica que los valores del gráfico deben dividirse por un divisor definido por el usuario. Este valor no es compatible con los nuevos tipos de gráfico de MS Office 2016.

### HUNDREDS {#HUNDREDS}
```
public static int HUNDREDS
```


Especifica que los valores del gráfico se dividirán por 100.

### HUNDRED_MILLIONS {#HUNDRED-MILLIONS}
```
public static int HUNDRED_MILLIONS
```


Especifica que los valores del gráfico se dividirán por 100,000,000.

### HUNDRED_THOUSANDS {#HUNDRED-THOUSANDS}
```
public static int HUNDRED_THOUSANDS
```


Especifica que los valores del gráfico se dividirán por 100,000.

### MILLIONS {#MILLIONS}
```
public static int MILLIONS
```


Especifica que los valores del gráfico se dividirán por 1,000,000.

### NONE {#NONE}
```
public static int NONE
```


Especifica que los valores del gráfico se mostrarán tal como están.

### PERCENTAGE {#PERCENTAGE}
```
public static int PERCENTAGE
```


Especifica que los valores del gráfico deben dividirse por 0.01. Este valor es compatible solo con los nuevos tipos de gráfico de MS Office 2016.

### TEN_MILLIONS {#TEN-MILLIONS}
```
public static int TEN_MILLIONS
```


Especifica que los valores del gráfico se dividirán por 10,000,000.

### TEN_THOUSANDS {#TEN-THOUSANDS}
```
public static int TEN_THOUSANDS
```


Especifica que los valores del gráfico se dividirán por 10,000.

### THOUSANDS {#THOUSANDS}
```
public static int THOUSANDS
```


Especifica que los valores del gráfico se dividirán por 1,000.

### TRILLIONS {#TRILLIONS}
```
public static int TRILLIONS
```


Especifica que los valores del gráfico se dividirán por 1,000,000,000,0000.

### length {#length}
```
public static int length
```


### fromName(String axisBuiltInUnitName) {#fromName-java.lang.String}
```
public static int fromName(String axisBuiltInUnitName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| axisBuiltInUnitName | java.lang.String |  |

**Returns:**
int
### getName(int axisBuiltInUnit) {#getName-int}
```
public static String getName(int axisBuiltInUnit)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| axisBuiltInUnit | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int axisBuiltInUnit) {#toString-int}
```
public static String toString(int axisBuiltInUnit)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| axisBuiltInUnit | int |  |

**Returns:**
java.lang.String
