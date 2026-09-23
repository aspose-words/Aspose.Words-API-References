---
title: "AxisBuiltInUnit"
linktitle: "AxisBuiltInUnit"
second_title: "Aspose.Words für Java"
description: "Gibt die Anzeigeeinheiten für eine Achse in Java an."
type: docs
weight: 23
url: /de/java/com.aspose.words/axisbuiltinunit/
---

**Inheritance:**
java.lang.Object
```
public class AxisBuiltInUnit
```

Gibt die Anzeigeeinheiten für eine Achse an.

 **Examples:** 

Zeigt, wie die Markierungen und angezeigten Werte einer Diagrammachse manipuliert werden können.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BILLIONS](#BILLIONS) | Gibt an, dass die Werte im Diagramm durch 1 000 000 000 geteilt werden. |
| [CUSTOM](#CUSTOM) | Gibt an, dass die Werte im Diagramm durch einen benutzerdefinierten Divisor geteilt werden. |
| [HUNDREDS](#HUNDREDS) | Gibt an, dass die Werte im Diagramm durch 100 geteilt werden. |
| [HUNDRED_MILLIONS](#HUNDRED-MILLIONS) | Gibt an, dass die Werte im Diagramm durch 100 000 000 geteilt werden. |
| [HUNDRED_THOUSANDS](#HUNDRED-THOUSANDS) | Gibt an, dass die Werte im Diagramm durch 100 000 geteilt werden. |
| [MILLIONS](#MILLIONS) | Gibt an, dass die Werte im Diagramm durch 1 000 000 geteilt werden. |
| [NONE](#NONE) | Gibt an, dass die Werte im Diagramm unverändert angezeigt werden. |
| [PERCENTAGE](#PERCENTAGE) | Gibt an, dass die Werte im Diagramm durch 0,01 geteilt werden. |
| [TEN_MILLIONS](#TEN-MILLIONS) | Gibt an, dass die Werte im Diagramm durch 10 000 000 geteilt werden. |
| [TEN_THOUSANDS](#TEN-THOUSANDS) | Gibt an, dass die Werte im Diagramm durch 10 000 geteilt werden. |
| [THOUSANDS](#THOUSANDS) | Gibt an, dass die Werte im Diagramm durch 1 000 geteilt werden. |
| [TRILLIONS](#TRILLIONS) | Gibt an, dass die Werte im Diagramm durch 1 000 000 000 0000 geteilt werden. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String axisBuiltInUnitName)](#fromName-java.lang.String) |  |
| [getName(int axisBuiltInUnit)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisBuiltInUnit)](#toString-int) |  |
### BILLIONS {#BILLIONS}
```
public static int BILLIONS
```


Gibt an, dass die Werte im Diagramm durch 1 000 000 000 geteilt werden.

### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Gibt an, dass die Werte im Diagramm durch einen benutzerdefinierten Divisor geteilt werden. Dieser Wert wird von den neuen Diagrammtypen von MS Office 2016 nicht unterstützt.

### HUNDREDS {#HUNDREDS}
```
public static int HUNDREDS
```


Gibt an, dass die Werte im Diagramm durch 100 geteilt werden.

### HUNDRED_MILLIONS {#HUNDRED-MILLIONS}
```
public static int HUNDRED_MILLIONS
```


Gibt an, dass die Werte im Diagramm durch 100 000 000 geteilt werden.

### HUNDRED_THOUSANDS {#HUNDRED-THOUSANDS}
```
public static int HUNDRED_THOUSANDS
```


Gibt an, dass die Werte im Diagramm durch 100 000 geteilt werden.

### MILLIONS {#MILLIONS}
```
public static int MILLIONS
```


Gibt an, dass die Werte im Diagramm durch 1 000 000 geteilt werden.

### NONE {#NONE}
```
public static int NONE
```


Gibt an, dass die Werte im Diagramm unverändert angezeigt werden.

### PERCENTAGE {#PERCENTAGE}
```
public static int PERCENTAGE
```


Gibt an, dass die Werte im Diagramm durch 0,01 geteilt werden. Dieser Wert wird nur von den neuen Diagrammtypen von MS Office 2016 unterstützt.

### TEN_MILLIONS {#TEN-MILLIONS}
```
public static int TEN_MILLIONS
```


Gibt an, dass die Werte im Diagramm durch 10 000 000 geteilt werden.

### TEN_THOUSANDS {#TEN-THOUSANDS}
```
public static int TEN_THOUSANDS
```


Gibt an, dass die Werte im Diagramm durch 10 000 geteilt werden.

### THOUSANDS {#THOUSANDS}
```
public static int THOUSANDS
```


Gibt an, dass die Werte im Diagramm durch 1 000 geteilt werden.

### TRILLIONS {#TRILLIONS}
```
public static int TRILLIONS
```


Gibt an, dass die Werte im Diagramm durch 1 000 000 000 0000 geteilt werden.

### length {#length}
```
public static int length
```


### fromName(String axisBuiltInUnitName) {#fromName-java.lang.String}
```
public static int fromName(String axisBuiltInUnitName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| axisBuiltInUnitName | java.lang.String |  |

**Returns:**
int
### getName(int axisBuiltInUnit) {#getName-int}
```
public static String getName(int axisBuiltInUnit)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| axisBuiltInUnit | int |  |

**Returns:**
java.lang.String
