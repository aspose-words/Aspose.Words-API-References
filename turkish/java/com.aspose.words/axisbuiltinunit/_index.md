---
title: "AxisBuiltInUnit"
linktitle: "AxisBuiltInUnit"
second_title: "Aspose.Words Java için"
description: "Java'da bir eksen için görüntüleme birimlerini belirtir."
type: docs
weight: 23
url: /tr/java/com.aspose.words/axisbuiltinunit/
---

**Inheritance:**
java.lang.Object
```
public class AxisBuiltInUnit
```

Bir eksen için görüntüleme birimlerini belirtir.

 **Examples:** 

Bir grafik ekseninin işaretçiklerini ve görüntülenen değerlerini nasıl manipüle edeceğinizi gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BILLIONS](#BILLIONS) | Grafikteki değerlerin 1.000.000.000 ile bölüneceğini belirtir. |
| [CUSTOM](#CUSTOM) | Grafikteki değerlerin kullanıcı tanımlı bir bölenle bölüneceğini belirtir. |
| [HUNDREDS](#HUNDREDS) | Grafikteki değerlerin 100 ile bölüneceğini belirtir. |
| [HUNDRED_MILLIONS](#HUNDRED-MILLIONS) | Grafikteki değerlerin 100.000.000 ile bölüneceğini belirtir. |
| [HUNDRED_THOUSANDS](#HUNDRED-THOUSANDS) | Grafikteki değerlerin 100.000 ile bölüneceğini belirtir. |
| [MILLIONS](#MILLIONS) | Grafikteki değerlerin 1.000.000 ile bölüneceğini belirtir. |
| [NONE](#NONE) | Grafikteki değerlerin olduğu gibi görüntüleneceğini belirtir. |
| [PERCENTAGE](#PERCENTAGE) | Grafikteki değerlerin 0,01 ile bölüneceğini belirtir. |
| [TEN_MILLIONS](#TEN-MILLIONS) | Grafikteki değerlerin 10.000.000 ile bölüneceğini belirtir. |
| [TEN_THOUSANDS](#TEN-THOUSANDS) | Grafikteki değerlerin 10.000 ile bölüneceğini belirtir. |
| [THOUSANDS](#THOUSANDS) | Grafikteki değerlerin 1.000 ile bölüneceğini belirtir. |
| [TRILLIONS](#TRILLIONS) | Grafikteki değerlerin 1,000,000,000,0000 ile bölüneceğini belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String axisBuiltInUnitName)](#fromName-java.lang.String) |  |
| [getName(int axisBuiltInUnit)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisBuiltInUnit)](#toString-int) |  |
### BILLIONS {#BILLIONS}
```
public static int BILLIONS
```


Grafikteki değerlerin 1.000.000.000 ile bölüneceğini belirtir.

### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Grafikteki değerlerin kullanıcı tanımlı bir bölenle bölüneceğini belirtir. Bu değer, MS Office 2016'nın yeni grafik türleri tarafından desteklenmez.

### HUNDREDS {#HUNDREDS}
```
public static int HUNDREDS
```


Grafikteki değerlerin 100 ile bölüneceğini belirtir.

### HUNDRED_MILLIONS {#HUNDRED-MILLIONS}
```
public static int HUNDRED_MILLIONS
```


Grafikteki değerlerin 100.000.000 ile bölüneceğini belirtir.

### HUNDRED_THOUSANDS {#HUNDRED-THOUSANDS}
```
public static int HUNDRED_THOUSANDS
```


Grafikteki değerlerin 100.000 ile bölüneceğini belirtir.

### MILLIONS {#MILLIONS}
```
public static int MILLIONS
```


Grafikteki değerlerin 1.000.000 ile bölüneceğini belirtir.

### NONE {#NONE}
```
public static int NONE
```


Grafikteki değerlerin olduğu gibi görüntüleneceğini belirtir.

### PERCENTAGE {#PERCENTAGE}
```
public static int PERCENTAGE
```


Grafikteki değerlerin 0,01 ile bölüneceğini belirtir. Bu değer yalnızca MS Office 2016'nın yeni grafik türleri tarafından desteklenir.

### TEN_MILLIONS {#TEN-MILLIONS}
```
public static int TEN_MILLIONS
```


Grafikteki değerlerin 10.000.000 ile bölüneceğini belirtir.

### TEN_THOUSANDS {#TEN-THOUSANDS}
```
public static int TEN_THOUSANDS
```


Grafikteki değerlerin 10.000 ile bölüneceğini belirtir.

### THOUSANDS {#THOUSANDS}
```
public static int THOUSANDS
```


Grafikteki değerlerin 1.000 ile bölüneceğini belirtir.

### TRILLIONS {#TRILLIONS}
```
public static int TRILLIONS
```


Grafikteki değerlerin 1,000,000,000,0000 ile bölüneceğini belirtir.

### length {#length}
```
public static int length
```


### fromName(String axisBuiltInUnitName) {#fromName-java.lang.String}
```
public static int fromName(String axisBuiltInUnitName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| axisBuiltInUnitName | java.lang.String |  |

**Returns:**
int
### getName(int axisBuiltInUnit) {#getName-int}
```
public static String getName(int axisBuiltInUnit)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| axisBuiltInUnit | int |  |

**Returns:**
java.lang.String
