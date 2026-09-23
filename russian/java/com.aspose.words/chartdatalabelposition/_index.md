---
title: "ChartDataLabelPosition"
linktitle: "ChartDataLabelPosition"
second_title: "Aspose.Words для Java"
description: "Указывает позицию подписи данных диаграммы в Java."
type: docs
weight: 74
url: /ru/java/com.aspose.words/chartdatalabelposition/
---

**Inheritance:**
java.lang.Object
```
public class ChartDataLabelPosition
```

Указывает позицию подписи данных диаграммы.

 **Remarks:** 

Не все типы рядов позволяют задавать позиции подписей. И те, которые позволяют, не поддерживают все значения.

 **Examples:** 

Показывает, как установить позицию подписи данных.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert column chart.
 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();

 // Delete default generated series.
 seriesColl.clear();

 // Add series.
 ChartSeries series = seriesColl.add(
         "Series 1",
         new String[] { "Category 1", "Category 2", "Category 3" },
         new double[] { 4.0, 5.0, 6.0 });

 // Show data labels and set font color.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.getFont().setColor(Color.WHITE);

 // Set data label position.
 dataLabels.setPosition(ChartDataLabelPosition.INSIDE_BASE);
 dataLabels.get(0).setPosition(ChartDataLabelPosition.OUTSIDE_END);
 dataLabels.get(0).getFont().setColor(Color.RED);

 doc.save(getArtifactsDir() + "Charts.LabelPosition.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [ABOVE](#ABOVE) | Указывает, что подпись данных должна отображаться над маркером данных. |
| [BELOW](#BELOW) | Указывает, что подпись данных должна отображаться под маркером данных. |
| [BEST_FIT](#BEST-FIT) | Указывает, что подпись данных должна отображаться в наиболее подходящей позиции. |
| [CENTER](#CENTER) | Указывает, что подпись данных должна отображаться по центру маркера данных. |
| [INSIDE_BASE](#INSIDE-BASE) | Указывает, что подпись данных должна отображаться внутри основания маркера данных. |
| [INSIDE_END](#INSIDE-END) | Указывает, что подпись данных должна отображаться внутри конца маркера данных. |
| [LEFT](#LEFT) | Указывает, что подпись данных должна отображаться слева от маркера данных. |
| [OUTSIDE_END](#OUTSIDE-END) | Указывает, что подпись данных должна отображаться снаружи конца маркера данных. |
| [RIGHT](#RIGHT) | Указывает, что подпись данных должна отображаться справа от маркера данных. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String chartDataLabelPositionName)](#fromName-java.lang.String) |  |
| [getName(int chartDataLabelPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartDataLabelPosition)](#toString-int) |  |
### ABOVE {#ABOVE}
```
public static int ABOVE
```


Указывает, что подпись данных должна отображаться над маркером данных.

### BELOW {#BELOW}
```
public static int BELOW
```


Указывает, что подпись данных должна отображаться под маркером данных.

### BEST_FIT {#BEST-FIT}
```
public static int BEST_FIT
```


Указывает, что подпись данных должна отображаться в наиболее подходящей позиции.

### CENTER {#CENTER}
```
public static int CENTER
```


Указывает, что подпись данных должна отображаться по центру маркера данных.

### INSIDE_BASE {#INSIDE-BASE}
```
public static int INSIDE_BASE
```


Указывает, что подпись данных должна отображаться внутри основания маркера данных.

### INSIDE_END {#INSIDE-END}
```
public static int INSIDE_END
```


Указывает, что подпись данных должна отображаться внутри конца маркера данных.

### LEFT {#LEFT}
```
public static int LEFT
```


Указывает, что подпись данных должна отображаться слева от маркера данных.

### OUTSIDE_END {#OUTSIDE-END}
```
public static int OUTSIDE_END
```


Указывает, что подпись данных должна отображаться снаружи конца маркера данных.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Указывает, что подпись данных должна отображаться справа от маркера данных.

### length {#length}
```
public static int length
```


### fromName(String chartDataLabelPositionName) {#fromName-java.lang.String}
```
public static int fromName(String chartDataLabelPositionName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartDataLabelPositionName | java.lang.String |  |

**Returns:**
int
### getName(int chartDataLabelPosition) {#getName-int}
```
public static String getName(int chartDataLabelPosition)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartDataLabelPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartDataLabelPosition) {#toString-int}
```
public static String toString(int chartDataLabelPosition)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartDataLabelPosition | int |  |

**Returns:**
java.lang.String
