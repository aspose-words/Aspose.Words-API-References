---
title: "AxisBuiltInUnit"
linktitle: "AxisBuiltInUnit"
second_title: "Aspose.Words لـ Java"
description: "يحدد وحدات العرض للمحور في Java."
type: docs
weight: 23
url: /ar/java/com.aspose.words/axisbuiltinunit/
---

**Inheritance:**
java.lang.Object
```
public class AxisBuiltInUnit
```

يحدد وحدات العرض للمحور.

 **Examples:** 

يظهر كيفية تعديل علامات الفواصل والقيم المعروضة لمحور المخطط.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [BILLIONS](#BILLIONS) | يحدد أن القيم في المخطط ستقسم على 1,000,000,000. |
| [CUSTOM](#CUSTOM) | يحدد أن القيم في المخطط ستقسم على مقسّم يحدده المستخدم. |
| [HUNDREDS](#HUNDREDS) | يحدد أن القيم في المخطط ستقسم على 100. |
| [HUNDRED_MILLIONS](#HUNDRED-MILLIONS) | يحدد أن القيم في المخطط ستقسم على 100,000,000. |
| [HUNDRED_THOUSANDS](#HUNDRED-THOUSANDS) | يحدد أن القيم في المخطط ستقسم على 100,000. |
| [MILLIONS](#MILLIONS) | يحدد أن القيم في المخطط ستقسم على 1,000,000. |
| [NONE](#NONE) | يحدد أن القيم في المخطط ستُعرض كما هي. |
| [PERCENTAGE](#PERCENTAGE) | يحدد أن القيم في المخطط ستقسم على 0.01. |
| [TEN_MILLIONS](#TEN-MILLIONS) | يحدد أن القيم في المخطط ستقسم على 10,000,000. |
| [TEN_THOUSANDS](#TEN-THOUSANDS) | يحدد أن القيم في المخطط ستقسم على 10,000. |
| [THOUSANDS](#THOUSANDS) | يحدد أن القيم في المخطط ستقسم على 1,000. |
| [TRILLIONS](#TRILLIONS) | يحدد أن القيم في المخطط ستقسم على 1,000,000,000,0000. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String axisBuiltInUnitName)](#fromName-java.lang.String) |  |
| [getName(int axisBuiltInUnit)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisBuiltInUnit)](#toString-int) |  |
### BILLIONS {#BILLIONS}
```
public static int BILLIONS
```


يحدد أن القيم في المخطط ستقسم على 1,000,000,000.

### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


يحدد أن القيم في المخطط يجب أن تُقسم على قاسم يحدده المستخدم. هذه القيمة غير مدعومة من قبل أنواع المخططات الجديدة في MS Office 2016.

### HUNDREDS {#HUNDREDS}
```
public static int HUNDREDS
```


يحدد أن القيم في المخطط ستقسم على 100.

### HUNDRED_MILLIONS {#HUNDRED-MILLIONS}
```
public static int HUNDRED_MILLIONS
```


يحدد أن القيم في المخطط ستقسم على 100,000,000.

### HUNDRED_THOUSANDS {#HUNDRED-THOUSANDS}
```
public static int HUNDRED_THOUSANDS
```


يحدد أن القيم في المخطط ستقسم على 100,000.

### MILLIONS {#MILLIONS}
```
public static int MILLIONS
```


يحدد أن القيم في المخطط ستقسم على 1,000,000.

### NONE {#NONE}
```
public static int NONE
```


يحدد أن القيم في المخطط ستُعرض كما هي.

### PERCENTAGE {#PERCENTAGE}
```
public static int PERCENTAGE
```


يحدد أن القيم في المخطط يجب أن تُقسم على 0.01. هذه القيمة مدعومة فقط من قبل أنواع المخططات الجديدة في MS Office 2016.

### TEN_MILLIONS {#TEN-MILLIONS}
```
public static int TEN_MILLIONS
```


يحدد أن القيم في المخطط ستقسم على 10,000,000.

### TEN_THOUSANDS {#TEN-THOUSANDS}
```
public static int TEN_THOUSANDS
```


يحدد أن القيم في المخطط ستقسم على 10,000.

### THOUSANDS {#THOUSANDS}
```
public static int THOUSANDS
```


يحدد أن القيم في المخطط ستقسم على 1,000.

### TRILLIONS {#TRILLIONS}
```
public static int TRILLIONS
```


يحدد أن القيم في المخطط ستقسم على 1,000,000,000,0000.

### length {#length}
```
public static int length
```


### fromName(String axisBuiltInUnitName) {#fromName-java.lang.String}
```
public static int fromName(String axisBuiltInUnitName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| axisBuiltInUnitName | java.lang.String |  |

**Returns:**
int
### getName(int axisBuiltInUnit) {#getName-int}
```
public static String getName(int axisBuiltInUnit)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| axisBuiltInUnit | int |  |

**Returns:**
java.lang.String
