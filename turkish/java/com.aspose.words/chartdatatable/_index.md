---
title: "ChartDataTable"
linktitle: "ChartDataTable"
second_title: "Aspose.Words Java için"
description: "Java'da bir grafik veri tablosunun özelliklerini belirtmeye izin verir."
type: docs
weight: 77
url: /tr/java/com.aspose.words/chartdatatable/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartDataTable implements Cloneable
```

Grafik veri tablosunun özelliklerini belirtmeye izin verir.

 **Examples:** 

Grafik serisi verileriyle veri tablosunun nasıl gösterileceğini gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fetchSpecialDefaultRunPropertyValue(int key)](#fetchSpecialDefaultRunPropertyValue-int) |  |
| [generateItemText()](#generateItemText) |  |
| [getFont()](#getFont) | Veri tablosunun yazı tipi biçimlendirmesine erişim sağlar. |
| [getFormat()](#getFormat) | Veri tablosunun metin arka plan doldurmasına ve kenarlık biçimlendirmesine erişim sağlar. |
| [getRelativePropertyValue(int key, Object value)](#getRelativePropertyValue-int-java.lang.Object) |  |
| [getShapeType()](#getShapeType) |  |
| [getShow()](#getShow) | Grafik için veri tablosunun gösterilip gösterilmeyeceğini belirten bir bayrağı alır. |
| [hasHorizontalBorder()](#hasHorizontalBorder) | Veri tablosunun yatay kenarlığının gösterilip gösterilmediğini belirten bir bayrağı alır. |
| [hasHorizontalBorder(boolean value)](#hasHorizontalBorder-boolean) | Veri tablosunun yatay kenarlığının gösterilip gösterilmediğini belirten bir bayrağı ayarlar. |
| [hasLegendKeys()](#hasLegendKeys) | Veri tablosunda lejant anahtarlarının gösterilip gösterilmediğini belirten bir bayrağı alır. |
| [hasLegendKeys(boolean value)](#hasLegendKeys-boolean) | Veri tablosunda lejant anahtarlarının gösterilip gösterilmediğini belirten bir bayrağı ayarlar. |
| [hasOutlineBorder()](#hasOutlineBorder) | Seri ve kategori adlarının etrafındaki bir dış kenarlık, yani bir kontur kenarlığının gösterilip gösterilmediğini belirten bir bayrağı alır. |
| [hasOutlineBorder(boolean value)](#hasOutlineBorder-boolean) | Seri ve kategori adlarının etrafındaki bir dış kenarlık, yani bir kontur kenarlığının gösterilip gösterilmediğini belirten bir bayrağı ayarlar. |
| [hasVerticalBorder()](#hasVerticalBorder) | Veri tablosunun dikey kenarlığının gösterilip gösterilmediğini belirten bir bayrağı alır. |
| [hasVerticalBorder(boolean value)](#hasVerticalBorder-boolean) | Veri tablosunun dikey kenarlığının gösterilip gösterilmediğini belirten bir bayrağı ayarlar. |
| [isFillSupported()](#isFillSupported) |  |
| [isFormatDefined()](#isFormatDefined) |  |
| [materializeSpPr()](#materializeSpPr) |  |
| [setShapeType(int value)](#setShapeType-int) |  |
| [setShow(boolean value)](#setShow-boolean) | Grafik için veri tablosunun gösterilip gösterilmeyeceğini belirten bir bayrağı ayarlar. |
### fetchSpecialDefaultRunPropertyValue(int key) {#fetchSpecialDefaultRunPropertyValue-int}
```
public Object fetchSpecialDefaultRunPropertyValue(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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


Veri tablosunun yazı tipi biçimlendirmesine erişim sağlar.

 **Examples:** 

Grafik serisi verileriyle veri tablosunun nasıl gösterileceğini gösterir.

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


Veri tablosunun metin arka plan doldurmasına ve kenarlık biçimlendirmesine erişim sağlar.

 **Examples:** 

Grafik serisi verileriyle veri tablosunun nasıl gösterileceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| değer | java.lang.Object |  |

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


Grafik için veri tablosunun gösterilip gösterilmeyeceğini belirten bir bayrağı alır. Varsayılan değer false'tur.

 **Remarks:** 

Aşağıdaki grafik türleri veri tablolarını desteklemez: Scatter, Pie, Doughnut, Surface, Radar, Treemap, Sunburst, Histogram, Pareto, Box and Whisker, Waterfall, Funnel, bu tür serileri içeren Combo grafikler. Bu grafik türleri için bir veri tablosu gösterilmesi java.lang.IllegalStateException istisnası fırlatır.

 **Examples:** 

Grafik serisi verileriyle veri tablosunun nasıl gösterileceğini gösterir.

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
boolean - Grafik için veri tablosunun gösterilip gösterilmeyeceğini belirten bir bayrak.
### hasHorizontalBorder() {#hasHorizontalBorder}
```
public boolean hasHorizontalBorder()
```


Veri tablosunun yatay kenarlığının gösterilip gösterilmediğini belirten bir bayrağı alır. Varsayılan değer true'dur.

 **Examples:** 

Grafik serisi verileriyle veri tablosunun nasıl gösterileceğini gösterir.

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
boolean - Veri tablosunun yatay kenarlığının gösterilip gösterilmediğini belirten bir bayrak.
### hasHorizontalBorder(boolean value) {#hasHorizontalBorder-boolean}
```
public void hasHorizontalBorder(boolean value)
```


Veri tablosunun yatay kenarlığının gösterilip gösterilmediğini belirten bir bayrağı ayarlar. Varsayılan değer true'dur.

 **Examples:** 

Grafik serisi verileriyle veri tablosunun nasıl gösterileceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Veri tablosunun yatay kenarlığının gösterilip gösterilmediğini belirten bir bayrak. |

### hasLegendKeys() {#hasLegendKeys}
```
public boolean hasLegendKeys()
```


Veri tablosunda lejant anahtarlarının gösterilip gösterilmediğini belirten bir bayrağı alır. Varsayılan değer true'dur.

 **Examples:** 

Grafik serisi verileriyle veri tablosunun nasıl gösterileceğini gösterir.

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
boolean - Veri tablosunda lejant anahtarlarının gösterilip gösterilmediğini belirten bir bayrak.
### hasLegendKeys(boolean value) {#hasLegendKeys-boolean}
```
public void hasLegendKeys(boolean value)
```


Veri tablosunda lejant anahtarlarının gösterilip gösterilmediğini belirten bir bayrağı ayarlar. Varsayılan değer true'dur.

 **Examples:** 

Grafik serisi verileriyle veri tablosunun nasıl gösterileceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Veri tablosunda lejant anahtarlarının gösterilip gösterilmediğini belirten bir bayrak. |

### hasOutlineBorder() {#hasOutlineBorder}
```
public boolean hasOutlineBorder()
```


Bir bayrak alır; bu bayrak, seri ve kategori adlarının etrafındaki dış hat kenarlığının görüntülenip görüntülenmediğini gösterir. Varsayılan değer true.

 **Examples:** 

Grafik serisi verileriyle veri tablosunun nasıl gösterileceğini gösterir.

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
boolean - Bir dış hat kenarlığının, yani seri ve kategori adlarının etrafındaki kenarlığın görüntülenip görüntülenmediğini gösteren bayrak.
### hasOutlineBorder(boolean value) {#hasOutlineBorder-boolean}
```
public void hasOutlineBorder(boolean value)
```


Bir dış hat kenarlığının, yani seri ve kategori adlarının etrafındaki kenarlığın görüntülenip görüntülenmediğini gösteren bayrağı ayarlar. Varsayılan değer true.

 **Examples:** 

Grafik serisi verileriyle veri tablosunun nasıl gösterileceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Seri ve kategori adlarının etrafındaki dış hat kenarlığının görüntülenip görüntülenmediğini gösteren bayrak. |

### hasVerticalBorder() {#hasVerticalBorder}
```
public boolean hasVerticalBorder()
```


Veri tablosunun dikey kenarlığının görüntülenip görüntülenmediğini gösteren bir bayrak alır. Varsayılan değer true.

 **Examples:** 

Grafik serisi verileriyle veri tablosunun nasıl gösterileceğini gösterir.

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
boolean - Veri tablosunun dikey kenarlığının görüntülenip görüntülenmediğini gösteren bayrak.
### hasVerticalBorder(boolean value) {#hasVerticalBorder-boolean}
```
public void hasVerticalBorder(boolean value)
```


Veri tablosunun dikey kenarlığının görüntülenip görüntülenmediğini gösteren bir bayrak ayarlar. Varsayılan değer true.

 **Examples:** 

Grafik serisi verileriyle veri tablosunun nasıl gösterileceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Veri tablosunun dikey kenarlığının görüntülenip görüntülenmediğini gösteren bayrak. |

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int |  |

### setShow(boolean value) {#setShow-boolean}
```
public void setShow(boolean value)
```


Grafik için veri tablosunun gösterilip gösterilmeyeceğini belirten bir bayrak ayarlar. Varsayılan değer false.

 **Remarks:** 

Aşağıdaki grafik türleri veri tablolarını desteklemez: Scatter, Pie, Doughnut, Surface, Radar, Treemap, Sunburst, Histogram, Pareto, Box and Whisker, Waterfall, Funnel, bu tür serileri içeren Combo grafikler. Bu grafik türleri için bir veri tablosu gösterilmesi java.lang.IllegalStateException istisnası fırlatır.

 **Examples:** 

Grafik serisi verileriyle veri tablosunun nasıl gösterileceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Grafik için veri tablosunun gösterilip gösterilmeyeceğini belirten bayrak. |

