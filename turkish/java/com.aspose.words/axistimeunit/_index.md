---
title: "AxisTimeUnit"
linktitle: "AxisTimeUnit"
second_title: "Aspose.Words Java için"
description: "Java'da eksenler için zaman birimini belirtir."
type: docs
weight: 33
url: /tr/java/com.aspose.words/axistimeunit/
---

**Inheritance:**
java.lang.Object
```
public class AxisTimeUnit
```

Eksenler için zaman birimini belirtir.

 **Examples:** 

Tarih/saat değerleriyle bir grafik eklemenin nasıl yapılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AUTOMATIC](#AUTOMATIC) | Birim açıkça ayarlanmamış ve varsayılan değerin kullanılacağını belirtir. |
| [DAYS](#DAYS) | Grafik verilerinin gün cinsinden gösterileceğini belirtir. |
| [MONTHS](#MONTHS) | Grafik verilerinin ay cinsinden gösterileceğini belirtir. |
| [YEARS](#YEARS) | Grafik verilerinin yıl cinsinden gösterileceğini belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String axisTimeUnitName)](#fromName-java.lang.String) |  |
| [getName(int axisTimeUnit)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisTimeUnit)](#toString-int) |  |
### AUTOMATIC {#AUTOMATIC}
```
public static int AUTOMATIC
```


Birim açıkça ayarlanmamış ve varsayılan değerin kullanılacağını belirtir.

### DAYS {#DAYS}
```
public static int DAYS
```


Grafik verilerinin gün cinsinden gösterileceğini belirtir.

### MONTHS {#MONTHS}
```
public static int MONTHS
```


Grafik verilerinin ay cinsinden gösterileceğini belirtir.

### YEARS {#YEARS}
```
public static int YEARS
```


Grafik verilerinin yıl cinsinden gösterileceğini belirtir.

### length {#length}
```
public static int length
```


### fromName(String axisTimeUnitName) {#fromName-java.lang.String}
```
public static int fromName(String axisTimeUnitName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| axisTimeUnitName | java.lang.String |  |

**Returns:**
int
### getName(int axisTimeUnit) {#getName-int}
```
public static String getName(int axisTimeUnit)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| axisTimeUnit | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int axisTimeUnit) {#toString-int}
```
public static String toString(int axisTimeUnit)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| axisTimeUnit | int |  |

**Returns:**
java.lang.String
