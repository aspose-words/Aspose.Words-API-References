---
title: "LegendPosition"
linktitle: "LegendPosition"
second_title: "Aspose.Words для Java"
description: "Указывает возможные положения легенды диаграммы в Java."
type: docs
weight: 420
url: /ru/java/com.aspose.words/legendposition/
---

**Inheritance:**
java.lang.Object
```
public class LegendPosition
```

Указывает возможные позиции для легенды диаграммы.

 **Examples:** 

Показывает, как изменить внешний вид легенды диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // Move the chart's legend to the top right corner.
 ChartLegend legend = chart.getLegend();
 legend.setPosition(LegendPosition.TOP_RIGHT);

 // Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
 legend.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartLegend.docx");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [BOTTOM](#BOTTOM) | Указывает, что легенда должна быть нарисована внизу диаграммы. |
| [LEFT](#LEFT) | Указывает, что легенда должна быть нарисована слева от диаграммы. |
| [NONE](#NONE) | Легенда не будет отображаться на диаграмме. |
| [RIGHT](#RIGHT) | Указывает, что легенда должна быть нарисована справа от диаграммы. |
| [TOP](#TOP) | Указывает, что легенда должна быть нарисована вверху диаграммы. |
| [TOP_RIGHT](#TOP-RIGHT) | Указывает, что легенда должна быть нарисована в правом верхнем углу диаграммы. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String legendPositionName)](#fromName-java.lang.String) |  |
| [getName(int legendPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int legendPosition)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Указывает, что легенда должна быть нарисована внизу диаграммы.

### LEFT {#LEFT}
```
public static int LEFT
```


Указывает, что легенда должна быть нарисована слева от диаграммы.

### NONE {#NONE}
```
public static int NONE
```


Легенда не будет отображаться на диаграмме.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Указывает, что легенда должна быть нарисована справа от диаграммы.

### TOP {#TOP}
```
public static int TOP
```


Указывает, что легенда должна быть нарисована вверху диаграммы.

### TOP_RIGHT {#TOP-RIGHT}
```
public static int TOP_RIGHT
```


Указывает, что легенда должна быть нарисована в правом верхнем углу диаграммы.

### length {#length}
```
public static int length
```


### fromName(String legendPositionName) {#fromName-java.lang.String}
```
public static int fromName(String legendPositionName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| legendPositionName | java.lang.String |  |

**Returns:**
int
### getName(int legendPosition) {#getName-int}
```
public static String getName(int legendPosition)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| legendPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int legendPosition) {#toString-int}
```
public static String toString(int legendPosition)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| legendPosition | int |  |

**Returns:**
java.lang.String
