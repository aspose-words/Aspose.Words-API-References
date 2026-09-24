---
title: "AxisTickLabels"
linktitle: "AxisTickLabels"
second_title: "Aspose.Words Java için"
description: "Java'da eksen işaret işareti etiketlerinin özelliklerini temsil eder."
type: docs
weight: 31
url: /tr/java/com.aspose.words/axisticklabels/
---

**Inheritance:**
java.lang.Object
```
public class AxisTickLabels
```

Eksen tik işareti etiketlerinin özelliklerini temsil eder.

 **Examples:** 

Bir grafik eklemeyi ve eksenlerinin görünümünü değiştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 Assert.assertEquals(doc, xAxis.getDocument());

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);
 yAxis.getTickLabels().setAlignment(ParagraphAlignment.CENTER);
 yAxis.getTickLabels().getFont().setColor(Color.RED);
 yAxis.getTickLabels().setSpacing(1);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fetchSpecialDefaultRunPropertyValue(int key)](#fetchSpecialDefaultRunPropertyValue-int) |  |
| [generateItemText()](#generateItemText) |  |
| [getAlignment()](#getAlignment) | Eksen işaret etiketlerinin metin hizalamasını alır. |
| [getFont()](#getFont) | İşaret etiketlerinin yazı tipi biçimlendirmesine erişim sağlar. |
| [getOffset()](#getOffset) | İşaret etiketlerinin eksenden uzaklığını alır. |
| [getOrientation()](#getOrientation) | İşaret etiketi metninin yönünü alır. |
| [getPosition()](#getPosition) | İşaret etiketlerinin eksen üzerindeki konumunu alır. |
| [getRelativePropertyValue(int key, Object value)](#getRelativePropertyValue-int-java.lang.Object) |  |
| [getRotation()](#getRotation) | İşaret etiketlerinin derece cinsinden dönüşünü alır. |
| [getSpacing()](#getSpacing) | İşaret etiketlerinin çizildiği aralığı alır. |
| [isAutoSpacing()](#isAutoSpacing) | İşaret etiketlerini çizerken otomatik aralık kullanılacağını gösteren bayrağı alır. |
| [isAutoSpacing(boolean value)](#isAutoSpacing-boolean) | İşaret etiketlerini çizerken otomatik aralık kullanılacağını gösteren bayrağı ayarlar. |
| [setAlignment(int value)](#setAlignment-int) | Eksen işaret etiketlerinin metin hizalamasını ayarlar. |
| [setOffset(int value)](#setOffset-int) | İşaret etiketlerinin eksenden uzaklığını ayarlar. |
| [setOrientation(int value)](#setOrientation-int) | İşaret etiketi metninin yönünü ayarlar. |
| [setPosition(int value)](#setPosition-int) | İşaret etiketlerinin eksen üzerindeki konumunu ayarlar. |
| [setRotation(int value)](#setRotation-int) | İşaret etiketlerinin derece cinsinden dönüşünü ayarlar. |
| [setSpacing(int value)](#setSpacing-int) | İşaret etiketlerinin çizildiği aralığı ayarlar. |
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
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Eksen işaret etiketlerinin metin hizalamasını alır.

 **Remarks:** 

Bu özellik yalnızca çok satırlı etiketler için etkilidir.

Varsayılan değer, [ParagraphAlignment.CENTER](../../com.aspose.words/paragraphalignment/\#CENTER) değeridir.

.

 **Examples:** 

Bir grafik eklemeyi ve eksenlerinin görünümünü değiştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 Assert.assertEquals(doc, xAxis.getDocument());

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);
 yAxis.getTickLabels().setAlignment(ParagraphAlignment.CENTER);
 yAxis.getTickLabels().getFont().setColor(Color.RED);
 yAxis.getTickLabels().setSpacing(1);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
int - Eksen işaret etiketlerinin metin hizalaması. Döndürülen değer, [ParagraphAlignment](../../com.aspose.words/paragraphalignment/) sabitlerinden biridir.
### getFont() {#getFont}
```
public Font getFont()
```


İşaret etiketlerinin yazı tipi biçimlendirmesine erişim sağlar.

 **Examples:** 

Bir grafik eklemeyi ve eksenlerinin görünümünü değiştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 Assert.assertEquals(doc, xAxis.getDocument());

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);
 yAxis.getTickLabels().setAlignment(ParagraphAlignment.CENTER);
 yAxis.getTickLabels().getFont().setColor(Color.RED);
 yAxis.getTickLabels().setSpacing(1);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getOffset() {#getOffset}
```
public int getOffset()
```


İşaret etiketlerinin eksenden uzaklığını alır.

 **Remarks:** 

Bu özellik, varsayılan etiket kaymasının bir yüzdesini temsil eder.

Geçerli aralık 0 ile 1000 yüzde dahilidir. Varsayılan değer %100'tür.

Bu özellik yalnızca kategori eksenleri için etkilidir. MS Office 2016 yeni grafiklerinde desteklenmez.

 **Examples:** 

Bir grafik eklemeyi ve eksenlerinin görünümünü değiştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 Assert.assertEquals(doc, xAxis.getDocument());

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);
 yAxis.getTickLabels().setAlignment(ParagraphAlignment.CENTER);
 yAxis.getTickLabels().getFont().setColor(Color.RED);
 yAxis.getTickLabels().setSpacing(1);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
int - İşaret etiketlerinin eksenden uzaklığı.
### getOrientation() {#getOrientation}
```
public int getOrientation()
```


İşaret etiketi metninin yönünü alır.

 **Remarks:** 

Varsayılan değer [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL) dir.

Bazı [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/) değerlerinin değer eksenlerindeki işaret etiketi metninin yönünü etkilemediğini unutmayın.

 **Examples:** 

Eksen işaret etiketleri için yön ve dönüşün nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a column chart.
 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 AxisTickLabels xTickLabels = shape.getChart().getAxisX().getTickLabels();
 AxisTickLabels yTickLabels = shape.getChart().getAxisY().getTickLabels();

 // Set axis tick label orientation and rotation.
 xTickLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 xTickLabels.setRotation(-30);
 yTickLabels.setOrientation(ShapeTextOrientation.HORIZONTAL);
 yTickLabels.setRotation(45);

 doc.save(getArtifactsDir() + "Charts.TickLabelsOrientationRotation.docx");
 
```

**Returns:**
int - İşaret etiketi metninin yönü. Döndürülen değer, [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/) sabitlerinden biridir.
### getPosition() {#getPosition}
```
public int getPosition()
```


İşaret etiketlerinin eksen üzerindeki konumunu alır.

 **Remarks:** 

Bu özellik MS Office 2016 yeni grafiklerinde desteklenmez.

 **Examples:** 

Bir grafik eklemeyi ve eksenlerinin görünümünü değiştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 Assert.assertEquals(doc, xAxis.getDocument());

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);
 yAxis.getTickLabels().setAlignment(ParagraphAlignment.CENTER);
 yAxis.getTickLabels().getFont().setColor(Color.RED);
 yAxis.getTickLabels().setSpacing(1);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
int - İşaret etiketlerinin eksen üzerindeki konumu. Döndürülen değer, [AxisTickLabelPosition](../../com.aspose.words/axisticklabelposition/) sabitlerinden biridir.
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
### getRotation() {#getRotation}
```
public int getRotation()
```


İşaret etiketlerinin derece cinsinden dönüşünü alır.

 **Remarks:** 

Kabul edilebilir değer aralığı -180 ile 180 arasında, dahil. Varsayılan değer 0'dır.

 **Examples:** 

Eksen işaret etiketleri için yön ve dönüşün nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a column chart.
 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 AxisTickLabels xTickLabels = shape.getChart().getAxisX().getTickLabels();
 AxisTickLabels yTickLabels = shape.getChart().getAxisY().getTickLabels();

 // Set axis tick label orientation and rotation.
 xTickLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 xTickLabels.setRotation(-30);
 yTickLabels.setOrientation(ShapeTextOrientation.HORIZONTAL);
 yTickLabels.setRotation(45);

 doc.save(getArtifactsDir() + "Charts.TickLabelsOrientationRotation.docx");
 
```

**Returns:**
int - İşaret etiketlerinin derece cinsinden dönüşü.
### getSpacing() {#getSpacing}
```
public int getSpacing()
```


İşaret etiketlerinin çizildiği aralığı alır.

 **Remarks:** 

Bu özellik metin kategori ve seri eksenleri için etkilidir. MS Office 2016 yeni grafiklerinde desteklenmez. Bir değerin geçerli aralığı 1 veya daha büyük olmalıdır.

Bu özelliği ayarlamak, [isAutoSpacing()](../../com.aspose.words/axisticklabels/\#isAutoSpacing) / [isAutoSpacing(boolean)](../../com.aspose.words/axisticklabels/\#isAutoSpacing-boolean) özelliğini false olarak ayarlar.

 **Examples:** 

Bir grafik eklemeyi ve eksenlerinin görünümünü değiştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 Assert.assertEquals(doc, xAxis.getDocument());

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);
 yAxis.getTickLabels().setAlignment(ParagraphAlignment.CENTER);
 yAxis.getTickLabels().getFont().setColor(Color.RED);
 yAxis.getTickLabels().setSpacing(1);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
int - İşaret etiketlerinin çizildiği aralık.
### isAutoSpacing() {#isAutoSpacing}
```
public boolean isAutoSpacing()
```


İşaret etiketlerini çizerken otomatik aralık kullanılacağını gösteren bayrağı alır.

 **Remarks:** 

Varsayılan değer  true .

Bu özellik metin kategori ve seri eksenleri için etkilidir. MS Office 2016 yeni grafiklerinde desteklenmez.

 **Examples:** 

Bir grafik eklemeyi ve eksenlerinin görünümünü değiştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 Assert.assertEquals(doc, xAxis.getDocument());

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);
 yAxis.getTickLabels().setAlignment(ParagraphAlignment.CENTER);
 yAxis.getTickLabels().getFont().setColor(Color.RED);
 yAxis.getTickLabels().setSpacing(1);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
boolean - İşaret etiketlerini çizerken otomatik aralık kullanılacağını gösteren bir işaret.
### isAutoSpacing(boolean value) {#isAutoSpacing-boolean}
```
public void isAutoSpacing(boolean value)
```


İşaret etiketlerini çizerken otomatik aralık kullanılacağını gösteren bayrağı ayarlar.

 **Remarks:** 

Varsayılan değer  true .

Bu özellik metin kategori ve seri eksenleri için etkilidir. MS Office 2016 yeni grafiklerinde desteklenmez.

 **Examples:** 

Bir grafik eklemeyi ve eksenlerinin görünümünü değiştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 Assert.assertEquals(doc, xAxis.getDocument());

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);
 yAxis.getTickLabels().setAlignment(ParagraphAlignment.CENTER);
 yAxis.getTickLabels().getFont().setColor(Color.RED);
 yAxis.getTickLabels().setSpacing(1);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İşaret etiketlerini çizerken otomatik aralık kullanılacağını gösteren bir işaret. |

### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Eksen işaret etiketlerinin metin hizalamasını ayarlar.

 **Remarks:** 

Bu özellik yalnızca çok satırlı etiketler için etkilidir.

Varsayılan değer, [ParagraphAlignment.CENTER](../../com.aspose.words/paragraphalignment/\#CENTER) değeridir.

.

 **Examples:** 

Bir grafik eklemeyi ve eksenlerinin görünümünü değiştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 Assert.assertEquals(doc, xAxis.getDocument());

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);
 yAxis.getTickLabels().setAlignment(ParagraphAlignment.CENTER);
 yAxis.getTickLabels().getFont().setColor(Color.RED);
 yAxis.getTickLabels().setSpacing(1);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Eksen işaret etiketlerinin metin hizalaması. Değer, [ParagraphAlignment](../../com.aspose.words/paragraphalignment/) sabitlerinden biri olmalıdır. |

### setOffset(int value) {#setOffset-int}
```
public void setOffset(int value)
```


İşaret etiketlerinin eksenden uzaklığını ayarlar.

 **Remarks:** 

Bu özellik, varsayılan etiket kaymasının bir yüzdesini temsil eder.

Geçerli aralık 0 ile 1000 yüzde dahilidir. Varsayılan değer %100'tür.

Bu özellik yalnızca kategori eksenleri için etkilidir. MS Office 2016 yeni grafiklerinde desteklenmez.

 **Examples:** 

Bir grafik eklemeyi ve eksenlerinin görünümünü değiştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 Assert.assertEquals(doc, xAxis.getDocument());

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);
 yAxis.getTickLabels().setAlignment(ParagraphAlignment.CENTER);
 yAxis.getTickLabels().getFont().setColor(Color.RED);
 yAxis.getTickLabels().setSpacing(1);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | İşaret etiketlerinin eksenden uzaklığı. |

### setOrientation(int value) {#setOrientation-int}
```
public void setOrientation(int value)
```


İşaret etiketi metninin yönünü ayarlar.

 **Remarks:** 

Varsayılan değer [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL) dir.

Bazı [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/) değerlerinin değer eksenlerindeki işaret etiketi metninin yönünü etkilemediğini unutmayın.

 **Examples:** 

Eksen işaret etiketleri için yön ve dönüşün nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a column chart.
 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 AxisTickLabels xTickLabels = shape.getChart().getAxisX().getTickLabels();
 AxisTickLabels yTickLabels = shape.getChart().getAxisY().getTickLabels();

 // Set axis tick label orientation and rotation.
 xTickLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 xTickLabels.setRotation(-30);
 yTickLabels.setOrientation(ShapeTextOrientation.HORIZONTAL);
 yTickLabels.setRotation(45);

 doc.save(getArtifactsDir() + "Charts.TickLabelsOrientationRotation.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İşaret etiketi metninin yönü. Değer, [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/) sabitlerinden biri olmalıdır. |

### setPosition(int value) {#setPosition-int}
```
public void setPosition(int value)
```


İşaret etiketlerinin eksen üzerindeki konumunu ayarlar.

 **Remarks:** 

Bu özellik MS Office 2016 yeni grafiklerinde desteklenmez.

 **Examples:** 

Bir grafik eklemeyi ve eksenlerinin görünümünü değiştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 Assert.assertEquals(doc, xAxis.getDocument());

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);
 yAxis.getTickLabels().setAlignment(ParagraphAlignment.CENTER);
 yAxis.getTickLabels().getFont().setColor(Color.RED);
 yAxis.getTickLabels().setSpacing(1);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İşaret etiketlerinin eksen üzerindeki konumu. Değer, [AxisTickLabelPosition](../../com.aspose.words/axisticklabelposition/) sabitlerinden biri olmalıdır. |

### setRotation(int value) {#setRotation-int}
```
public void setRotation(int value)
```


İşaret etiketlerinin derece cinsinden dönüşünü ayarlar.

 **Remarks:** 

Kabul edilebilir değer aralığı -180 ile 180 arasında, dahil. Varsayılan değer 0'dır.

 **Examples:** 

Eksen işaret etiketleri için yön ve dönüşün nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a column chart.
 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 AxisTickLabels xTickLabels = shape.getChart().getAxisX().getTickLabels();
 AxisTickLabels yTickLabels = shape.getChart().getAxisY().getTickLabels();

 // Set axis tick label orientation and rotation.
 xTickLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 xTickLabels.setRotation(-30);
 yTickLabels.setOrientation(ShapeTextOrientation.HORIZONTAL);
 yTickLabels.setRotation(45);

 doc.save(getArtifactsDir() + "Charts.TickLabelsOrientationRotation.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | İşaret etiketlerinin derece cinsinden dönüşü. |

### setSpacing(int value) {#setSpacing-int}
```
public void setSpacing(int value)
```


İşaret etiketlerinin çizildiği aralığı ayarlar.

 **Remarks:** 

Bu özellik metin kategori ve seri eksenleri için etkilidir. MS Office 2016 yeni grafiklerinde desteklenmez. Bir değerin geçerli aralığı 1 veya daha büyük olmalıdır.

Bu özelliği ayarlamak, [isAutoSpacing()](../../com.aspose.words/axisticklabels/\#isAutoSpacing) / [isAutoSpacing(boolean)](../../com.aspose.words/axisticklabels/\#isAutoSpacing-boolean) özelliğini false olarak ayarlar.

 **Examples:** 

Bir grafik eklemeyi ve eksenlerinin görünümünü değiştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 Assert.assertEquals(doc, xAxis.getDocument());

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);
 yAxis.getTickLabels().setAlignment(ParagraphAlignment.CENTER);
 yAxis.getTickLabels().getFont().setColor(Color.RED);
 yAxis.getTickLabels().setSpacing(1);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | İşaret etiketlerinin çizildiği aralık. |

