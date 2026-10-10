---
title: "ChartDataTable"
linktitle: "ChartDataTable"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد خصائص جدول بيانات المخطط في Java."
type: docs
weight: 77
url: /ar/java/com.aspose.words/chartdatatable/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartDataTable implements Cloneable
```

يسمح بتحديد خصائص جدول بيانات المخطط.

 **Examples:** 

يوضح كيفية إظهار جدول البيانات مع بيانات سلاسل المخطط.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fetchSpecialDefaultRunPropertyValue(int key)](#fetchSpecialDefaultRunPropertyValue-int) |  |
| [generateItemText()](#generateItemText) |  |
| [getFont()](#getFont) | يوفر الوصول إلى تنسيق الخط لجدول البيانات. |
| [getFormat()](#getFormat) | يوفر الوصول إلى تعبئة خلفية النص وتنسيق حدود جدول البيانات. |
| [getRelativePropertyValue(int key, Object value)](#getRelativePropertyValue-int-java.lang.Object) |  |
| [getShapeType()](#getShapeType) |  |
| [getShow()](#getShow) | يحصل على علم يشير إلى ما إذا كان سيتم عرض جدول البيانات للمخطط. |
| [hasHorizontalBorder()](#hasHorizontalBorder) | يحصل على علم يشير إلى ما إذا كان يتم عرض حد أفقي لجدول البيانات. |
| [hasHorizontalBorder(boolean value)](#hasHorizontalBorder-boolean) | يضبط علمًا يشير إلى ما إذا كان يتم عرض حد أفقي لجدول البيانات. |
| [hasLegendKeys()](#hasLegendKeys) | يحصل على علم يشير إلى ما إذا كانت مفاتيح الأسطورة معروضة في جدول البيانات. |
| [hasLegendKeys(boolean value)](#hasLegendKeys-boolean) | يضبط علمًا يشير إلى ما إذا كانت مفاتيح الأسطورة معروضة في جدول البيانات. |
| [hasOutlineBorder()](#hasOutlineBorder) | يحصل على علم يشير إلى ما إذا كان حدًا خارجيًا، أي حدًا حول أسماء السلاسل والفئات، معروضًا. |
| [hasOutlineBorder(boolean value)](#hasOutlineBorder-boolean) | يضبط علمًا يشير إلى ما إذا كان حدًا خارجيًا، أي حدًا حول أسماء السلاسل والفئات، معروضًا. |
| [hasVerticalBorder()](#hasVerticalBorder) | يحصل على علم يشير إلى ما إذا كان يتم عرض حد عمودي لجدول البيانات. |
| [hasVerticalBorder(boolean value)](#hasVerticalBorder-boolean) | يضبط علمًا يشير إلى ما إذا كان يتم عرض حد عمودي لجدول البيانات. |
| [isFillSupported()](#isFillSupported) |  |
| [isFormatDefined()](#isFormatDefined) |  |
| [materializeSpPr()](#materializeSpPr) |  |
| [setShapeType(int value)](#setShapeType-int) |  |
| [setShow(boolean value)](#setShow-boolean) | يضبط علمًا يشير إلى ما إذا كان سيتم عرض جدول البيانات للمخطط. |
### fetchSpecialDefaultRunPropertyValue(int key) {#fetchSpecialDefaultRunPropertyValue-int}
```
public Object fetchSpecialDefaultRunPropertyValue(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

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


يوفر الوصول إلى تنسيق الخط لجدول البيانات.

 **Examples:** 

يوضح كيفية إظهار جدول البيانات مع بيانات سلاسل المخطط.

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


يوفر الوصول إلى تعبئة خلفية النص وتنسيق حدود جدول البيانات.

 **Examples:** 

يوضح كيفية إظهار جدول البيانات مع بيانات سلاسل المخطط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| قيمة | java.lang.Object |  |

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


يحصل على علم يشير إلى ما إذا كان سيتم عرض جدول البيانات للمخطط. القيمة الافتراضية هي false.

 **Remarks:** 

الأنواع التالية من المخططات لا تدعم جداول البيانات: Scatter, Pie, Doughnut, Surface, Radar, Treemap, Sunburst, Histogram, Pareto, Box and Whisker, Waterfall, Funnel, المخططات المركبة التي تشمل سلاسل من هذه الأنواع. إظهار جدول بيانات لأنواع المخططات يثير استثناء java.lang.IllegalStateException.

 **Examples:** 

يوضح كيفية إظهار جدول البيانات مع بيانات سلاسل المخطط.

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
boolean - علم يشير إلى ما إذا كان سيتم عرض جدول البيانات للمخطط.
### hasHorizontalBorder() {#hasHorizontalBorder}
```
public boolean hasHorizontalBorder()
```


يحصل على علم يشير إلى ما إذا كان يتم عرض حد أفقي لجدول البيانات. القيمة الافتراضية هي true.

 **Examples:** 

يوضح كيفية إظهار جدول البيانات مع بيانات سلاسل المخطط.

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
boolean - علم يشير إلى ما إذا كان يتم عرض حد أفقي لجدول البيانات.
### hasHorizontalBorder(boolean value) {#hasHorizontalBorder-boolean}
```
public void hasHorizontalBorder(boolean value)
```


يضبط علمًا يشير إلى ما إذا كان يتم عرض حد أفقي لجدول البيانات. القيمة الافتراضية هي true.

 **Examples:** 

يوضح كيفية إظهار جدول البيانات مع بيانات سلاسل المخطط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علم يشير إلى ما إذا كان يتم عرض حد أفقي لجدول البيانات. |

### hasLegendKeys() {#hasLegendKeys}
```
public boolean hasLegendKeys()
```


يحصل على علم يشير إلى ما إذا كانت مفاتيح الأسطورة معروضة في جدول البيانات. القيمة الافتراضية هي true.

 **Examples:** 

يوضح كيفية إظهار جدول البيانات مع بيانات سلاسل المخطط.

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
boolean - علم يشير إلى ما إذا كانت مفاتيح الأسطورة معروضة في جدول البيانات.
### hasLegendKeys(boolean value) {#hasLegendKeys-boolean}
```
public void hasLegendKeys(boolean value)
```


يضبط علمًا يشير إلى ما إذا كانت مفاتيح الأسطورة معروضة في جدول البيانات. القيمة الافتراضية هي true.

 **Examples:** 

يوضح كيفية إظهار جدول البيانات مع بيانات سلاسل المخطط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علم يشير إلى ما إذا كانت مفاتيح الأسطورة معروضة في جدول البيانات. |

### hasOutlineBorder() {#hasOutlineBorder}
```
public boolean hasOutlineBorder()
```


يحصل على علم يشير إلى ما إذا كان يتم عرض حد خارجي، أي حد حول أسماء السلاسل والفئات. القيمة الافتراضية هي true.

 **Examples:** 

يوضح كيفية إظهار جدول البيانات مع بيانات سلاسل المخطط.

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
boolean - علم يشير إلى ما إذا كان يتم عرض حد خارجي، أي حد حول أسماء السلاسل والفئات.
### hasOutlineBorder(boolean value) {#hasOutlineBorder-boolean}
```
public void hasOutlineBorder(boolean value)
```


يضبط علمًا يشير إلى ما إذا كان يتم عرض حد خارجي، أي حد حول أسماء السلاسل والفئات. القيمة الافتراضية هي true.

 **Examples:** 

يوضح كيفية إظهار جدول البيانات مع بيانات سلاسل المخطط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علم يشير إلى ما إذا كان يتم عرض حد خارجي، أي حد حول أسماء السلاسل والفئات. |

### hasVerticalBorder() {#hasVerticalBorder}
```
public boolean hasVerticalBorder()
```


يحصل على علم يشير إلى ما إذا كان يتم عرض حد عمودي لجدول البيانات. القيمة الافتراضية هي true.

 **Examples:** 

يوضح كيفية إظهار جدول البيانات مع بيانات سلاسل المخطط.

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
boolean - علم يشير إلى ما إذا كان يتم عرض حد عمودي لجدول البيانات.
### hasVerticalBorder(boolean value) {#hasVerticalBorder-boolean}
```
public void hasVerticalBorder(boolean value)
```


يضبط علمًا يشير إلى ما إذا كان يتم عرض حد عمودي لجدول البيانات. القيمة الافتراضية هي true.

 **Examples:** 

يوضح كيفية إظهار جدول البيانات مع بيانات سلاسل المخطط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علم يشير إلى ما إذا كان يتم عرض حد عمودي لجدول البيانات. |

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int |  |

### setShow(boolean value) {#setShow-boolean}
```
public void setShow(boolean value)
```


يضبط علمًا يشير إلى ما إذا كان جدول البيانات سيظهر للمخطط. القيمة الافتراضية هي false.

 **Remarks:** 

الأنواع التالية من المخططات لا تدعم جداول البيانات: Scatter, Pie, Doughnut, Surface, Radar, Treemap, Sunburst, Histogram, Pareto, Box and Whisker, Waterfall, Funnel, المخططات المركبة التي تشمل سلاسل من هذه الأنواع. إظهار جدول بيانات لأنواع المخططات يثير استثناء java.lang.IllegalStateException.

 **Examples:** 

يوضح كيفية إظهار جدول البيانات مع بيانات سلاسل المخطط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علم يشير إلى ما إذا كان جدول البيانات سيظهر للمخطط. |

