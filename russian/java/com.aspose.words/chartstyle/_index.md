---
title: "ChartStyle"
linktitle: "ChartStyle"
second_title: "Aspose.Words для Java"
description: "Указывает предопределённые стили диаграммы в Java."
type: docs
weight: 91
url: /ru/java/com.aspose.words/chartstyle/
---

**Inheritance:**
java.lang.Object
```
public class ChartStyle
```

Указывает предопределённые стили диаграммы.

 **Examples:** 

Показывает, как установить и получить стиль диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a chart in the Black style.
 builder.insertChart(ChartType.COLUMN, 400.0, 250.0, ChartStyle.BLACK);

 doc.save(getArtifactsDir() + "Charts.SetChartStyle.docx");

 doc = new Document(getArtifactsDir() + "Charts.SetChartStyle.docx");

 // Get a chart to update.
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Chart chart = shape.getChart();

 // Get the chart style.
 Assert.assertEquals(ChartStyle.BLACK, chart.getStyle());
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [BLACK](#BLACK) | Стиль с чёрным фоном диаграммы. |
| [BLUE](#BLUE) | Стиль с синим фоном диаграммы. |
| [FLAT](#FLAT) | Стиль с плоскими точками данных без градиента. |
| [GRADIENT](#GRADIENT) | Стиль с градиентной заливкой точек данных. |
| [GREY](#GREY) | Стиль со светло-серым градиентным фоном диаграммы. |
| [MUTED](#MUTED) | Стиль с приглушёнными цветами. |
| [NORMAL](#NORMAL) | Представляет стиль диаграммы по умолчанию. |
| [ORIGINAL](#ORIGINAL) | Стиль с оригинальным внешним видом диаграммы. |
| [OUTLINE](#OUTLINE) | Стиль с точками данных без заливки, только с контуром. |
| [OUTLINE_BLACK](#OUTLINE-BLACK) | Стиль с черным фоном диаграммы, в котором точки данных без заливки, только с контуром. |
| [SATURATED](#SATURATED) | Стиль с более насыщенными цветами. |
| [SHADED](#SHADED) | Стиль с затененными точками данных. |
| [SHADED_PLOT](#SHADED-PLOT) | Стиль, в котором область построения затенена. |
| [SHADOWED](#SHADOWED) | Стиль с точками данных, имеющими тень. |
| [TRANSPARENT_1](#TRANSPARENT-1) | Стиль с прозрачными точками данных. |
| [TRANSPARENT_2](#TRANSPARENT-2) | Стиль с прозрачными точками данных. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String chartStyleName)](#fromName-java.lang.String) |  |
| [getName(int chartStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartStyle)](#toString-int) |  |
### BLACK {#BLACK}
```
public static int BLACK
```


Стиль с чёрным фоном диаграммы.

### BLUE {#BLUE}
```
public static int BLUE
```


Стиль с синим фоном диаграммы.

### FLAT {#FLAT}
```
public static int FLAT
```


Стиль с плоскими точками данных без градиента.

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


Стиль с градиентной заливкой точек данных.

### GREY {#GREY}
```
public static int GREY
```


Стиль со светло-серым градиентным фоном диаграммы.

### MUTED {#MUTED}
```
public static int MUTED
```


Стиль с приглушёнными цветами.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Представляет стиль диаграммы по умолчанию.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Стиль с оригинальным внешним видом диаграммы.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Стиль с точками данных без заливки, только с контуром.

### OUTLINE_BLACK {#OUTLINE-BLACK}
```
public static int OUTLINE_BLACK
```


Стиль с черным фоном диаграммы, в котором точки данных без заливки, только с контуром.

### SATURATED {#SATURATED}
```
public static int SATURATED
```


Стиль с более насыщенными цветами.

### SHADED {#SHADED}
```
public static int SHADED
```


Стиль с затененными точками данных.

### SHADED_PLOT {#SHADED-PLOT}
```
public static int SHADED_PLOT
```


Стиль, в котором область построения затенена.

### SHADOWED {#SHADOWED}
```
public static int SHADOWED
```


Стиль с точками данных, имеющими тень.

### TRANSPARENT_1 {#TRANSPARENT-1}
```
public static int TRANSPARENT_1
```


Стиль с прозрачными точками данных.

### TRANSPARENT_2 {#TRANSPARENT-2}
```
public static int TRANSPARENT_2
```


Стиль с прозрачными точками данных.

### length {#length}
```
public static int length
```


### fromName(String chartStyleName) {#fromName-java.lang.String}
```
public static int fromName(String chartStyleName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartStyleName | java.lang.String |  |

**Returns:**
int
### getName(int chartStyle) {#getName-int}
```
public static String getName(int chartStyle)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartStyle | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartStyle) {#toString-int}
```
public static String toString(int chartStyle)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartStyle | int |  |

**Returns:**
java.lang.String
