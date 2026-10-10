---
title: "ChartDataTable"
linktitle: "ChartDataTable"
second_title: "Aspose.Words для Java"
description: "Позволяет задавать свойства таблицы данных диаграммы в Java."
type: docs
weight: 77
url: /ru/java/com.aspose.words/chartdatatable/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartDataTable implements Cloneable
```

Позволяет указать свойства таблицы данных диаграммы.

 **Examples:** 

Показывает, как отобразить таблицу данных вместе с данными серий диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```
## Методы

| Метод | Описание |
| --- | --- |
| [fetchSpecialDefaultRunPropertyValue(int key)](#fetchSpecialDefaultRunPropertyValue-int) |  |
| [generateItemText()](#generateItemText) |  |
| [getFont()](#getFont) | Обеспечивает доступ к форматированию шрифта таблицы данных. |
| [getFormat()](#getFormat) | Обеспечивает доступ к заполнению фона текста и форматированию границы таблицы данных. |
| [getRelativePropertyValue(int key, Object value)](#getRelativePropertyValue-int-java.lang.Object) |  |
| [getShapeType()](#getShapeType) |  |
| [getShow()](#getShow) | Возвращает флаг, указывающий, будет ли таблица данных отображаться для диаграммы. |
| [hasHorizontalBorder()](#hasHorizontalBorder) | Возвращает флаг, указывающий, отображается ли горизонтальная граница таблицы данных. |
| [hasHorizontalBorder(boolean value)](#hasHorizontalBorder-boolean) | Устанавливает флаг, указывающий, отображается ли горизонтальная граница таблицы данных. |
| [hasLegendKeys()](#hasLegendKeys) | Возвращает флаг, указывающий, отображаются ли ключи легенды в таблице данных. |
| [hasLegendKeys(boolean value)](#hasLegendKeys-boolean) | Устанавливает флаг, указывающий, отображаются ли ключи легенды в таблице данных. |
| [hasOutlineBorder()](#hasOutlineBorder) | Возвращает флаг, указывающий, отображается ли контурная граница, то есть граница вокруг названий рядов и категорий. |
| [hasOutlineBorder(boolean value)](#hasOutlineBorder-boolean) | Устанавливает флаг, указывающий, отображается ли контурная граница, то есть граница вокруг названий рядов и категорий. |
| [hasVerticalBorder()](#hasVerticalBorder) | Возвращает флаг, указывающий, отображается ли вертикальная граница таблицы данных. |
| [hasVerticalBorder(boolean value)](#hasVerticalBorder-boolean) | Устанавливает флаг, указывающий, отображается ли вертикальная граница таблицы данных. |
| [isFillSupported()](#isFillSupported) |  |
| [isFormatDefined()](#isFormatDefined) |  |
| [materializeSpPr()](#materializeSpPr) |  |
| [setShapeType(int value)](#setShapeType-int) |  |
| [setShow(boolean value)](#setShow-boolean) | Устанавливает флаг, указывающий, будет ли таблица данных отображаться для диаграммы. |
### fetchSpecialDefaultRunPropertyValue(int key) {#fetchSpecialDefaultRunPropertyValue-int}
```
public Object fetchSpecialDefaultRunPropertyValue(int key)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ключ | int |  |

**Returns:**
java.lang.Object
### generateItemText() {#generateItemText}
```
public String generateItemText()
```




**Returns:**
java.lang.String
### getFont() {#getFont}
```
public Font getFont()
```


Обеспечивает доступ к форматированию шрифта таблицы данных.

 **Examples:** 

Показывает, как отобразить таблицу данных вместе с данными серий диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getFormat() {#getFormat}
```
public ChartFormat getFormat()
```


Обеспечивает доступ к заполнению фона текста и форматированию границы таблицы данных.

 **Examples:** 

Показывает, как отобразить таблицу данных вместе с данными серий диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Returns:**
[ChartFormat](../../com.aspose.words/chartformat/) - The corresponding [ChartFormat](../../com.aspose.words/chartformat/) value.
### getRelativePropertyValue(int key, Object value) {#getRelativePropertyValue-int-java.lang.Object}
```
public Object getRelativePropertyValue(int key, Object value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ключ | int |  |
| значение | java.lang.Object |  |

**Returns:**
java.lang.Object
### getShapeType() {#getShapeType}
```
public int getShapeType()
```




**Returns:**
int
### getShow() {#getShow}
```
public boolean getShow()
```


Возвращает флаг, указывающий, будет ли таблица данных отображаться для диаграммы. Значение по умолчанию — false.

 **Remarks:** 

Следующие типы диаграмм не поддерживают таблицы данных: Scatter, Pie, Doughnut, Surface, Radar, Treemap, Sunburst, Histogram, Pareto, Box and Whisker, Waterfall, Funnel, комбинированные диаграммы, содержащие серии этих типов. Показ таблицы данных для этих типов диаграмм вызывает исключение java.lang.IllegalStateException.

 **Examples:** 

Показывает, как отобразить таблицу данных вместе с данными серий диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Returns:**
boolean — Флаг, указывающий, будет ли таблица данных отображаться для диаграммы.
### hasHorizontalBorder() {#hasHorizontalBorder}
```
public boolean hasHorizontalBorder()
```


Возвращает флаг, указывающий, отображается ли горизонтальная граница таблицы данных. Значение по умолчанию — true.

 **Examples:** 

Показывает, как отобразить таблицу данных вместе с данными серий диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Returns:**
boolean — Флаг, указывающий, отображается ли горизонтальная граница таблицы данных.
### hasHorizontalBorder(boolean value) {#hasHorizontalBorder-boolean}
```
public void hasHorizontalBorder(boolean value)
```


Устанавливает флаг, указывающий, отображается ли горизонтальная граница таблицы данных. Значение по умолчанию — true.

 **Examples:** 

Показывает, как отобразить таблицу данных вместе с данными серий диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Флаг, указывающий, отображается ли горизонтальная граница таблицы данных. |

### hasLegendKeys() {#hasLegendKeys}
```
public boolean hasLegendKeys()
```


Возвращает флаг, указывающий, отображаются ли ключи легенды в таблице данных. Значение по умолчанию — true.

 **Examples:** 

Показывает, как отобразить таблицу данных вместе с данными серий диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Returns:**
boolean — Флаг, указывающий, отображаются ли ключи легенды в таблице данных.
### hasLegendKeys(boolean value) {#hasLegendKeys-boolean}
```
public void hasLegendKeys(boolean value)
```


Устанавливает флаг, указывающий, отображаются ли ключи легенды в таблице данных. Значение по умолчанию — true.

 **Examples:** 

Показывает, как отобразить таблицу данных вместе с данными серий диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Флаг, указывающий, отображаются ли ключи легенды в таблице данных. |

### hasOutlineBorder() {#hasOutlineBorder}
```
public boolean hasOutlineBorder()
```


Получает флаг, указывающий, отображается ли контурная граница, то есть граница вокруг названий серий и категорий. Значение по умолчанию —  true .

 **Examples:** 

Показывает, как отобразить таблицу данных вместе с данными серий диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Returns:**
boolean — Флаг, указывающий, отображается ли контурная граница, то есть граница вокруг названий серий и категорий.
### hasOutlineBorder(boolean value) {#hasOutlineBorder-boolean}
```
public void hasOutlineBorder(boolean value)
```


Устанавливает флаг, указывающий, отображается ли контурная граница, то есть граница вокруг названий серий и категорий. Значение по умолчанию —  true .

 **Examples:** 

Показывает, как отобразить таблицу данных вместе с данными серий диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Флаг, указывающий, отображается ли контурная граница, то есть граница вокруг названий серий и категорий. |

### hasVerticalBorder() {#hasVerticalBorder}
```
public boolean hasVerticalBorder()
```


Получает флаг, указывающий, отображается ли вертикальная граница таблицы данных. Значение по умолчанию —  true .

 **Examples:** 

Показывает, как отобразить таблицу данных вместе с данными серий диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Returns:**
boolean — Флаг, указывающий, отображается ли вертикальная граница таблицы данных.
### hasVerticalBorder(boolean value) {#hasVerticalBorder-boolean}
```
public void hasVerticalBorder(boolean value)
```


Устанавливает флаг, указывающий, отображается ли вертикальная граница таблицы данных. Значение по умолчанию —  true .

 **Examples:** 

Показывает, как отобразить таблицу данных вместе с данными серий диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Флаг, указывающий, отображается ли вертикальная граница таблицы данных. |

### isFillSupported() {#isFillSupported}
```
public boolean isFillSupported()
```




**Returns:**
boolean
### isFormatDefined() {#isFormatDefined}
```
public boolean isFormatDefined()
```




**Returns:**
boolean
### materializeSpPr() {#materializeSpPr}
```
public void materializeSpPr()
```




### setShapeType(int value) {#setShapeType-int}
```
public void setShapeType(int value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int |  |

### setShow(boolean value) {#setShow-boolean}
```
public void setShow(boolean value)
```


Устанавливает флаг, указывающий, будет ли таблица данных отображаться для диаграммы. Значение по умолчанию —  false .

 **Remarks:** 

Следующие типы диаграмм не поддерживают таблицы данных: Scatter, Pie, Doughnut, Surface, Radar, Treemap, Sunburst, Histogram, Pareto, Box and Whisker, Waterfall, Funnel, комбинированные диаграммы, содержащие серии этих типов. Показ таблицы данных для этих типов диаграмм вызывает исключение java.lang.IllegalStateException.

 **Examples:** 

Показывает, как отобразить таблицу данных вместе с данными серий диаграммы.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);
 dataTable.hasOutlineBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Флаг, указывающий, будет ли таблица данных отображаться для диаграммы. |

