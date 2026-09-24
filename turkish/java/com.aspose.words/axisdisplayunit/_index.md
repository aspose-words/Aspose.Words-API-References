---
title: "AxisDisplayUnit"
linktitle: "AxisDisplayUnit"
second_title: "Aspose.Words Java için"
description: "Java'da değer ekseni için görüntü birimlerinin ölçekleme seçeneklerine erişim sağlar."
type: docs
weight: 26
url: /tr/java/com.aspose.words/axisdisplayunit/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class AxisDisplayUnit implements Cloneable
```

Değer ekseni için görüntüleme birimlerinin ölçeklendirme seçeneklerine erişim sağlar.

Daha fazla bilgi için, [ Working with Charts ][Working with Charts] dokümantasyon makalesini ziyaret edin.

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


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getCustomUnit()](#getCustomUnit) | Değer eksenindeki görüntü birimlerini ölçeklemek için kullanıcı tanımlı bir bölen alır. |
| [getDefaultDisplayedFontSize()](#getDefaultDisplayedFontSize) |  |
| [getDefaultFontSize()](#getDefaultFontSize) |  |
| [getDefaultTitleText()](#getDefaultTitleText) |  |
| [getDocument()](#getDocument) | Üst grafiği içeren belgeyi döndürür. |
| [getRelativeFontSize(int chartFontSize)](#getRelativeFontSize-int) |  |
| [getStyleItem()](#getStyleItem) |  |
| [getTitleDeleted()](#getTitleDeleted) |  |
| [getTitlePosition()](#getTitlePosition) |  |
| [getUnit()](#getUnit) | Görüntü birimlerinin ölçekleme değerini önceden tanımlı değerlerden biri olarak alır. |
| [isVisible()](#isVisible) |  |
| [setCustomUnit(double value)](#setCustomUnit-double) | Değer eksenindeki görüntü birimlerini ölçeklemek için kullanıcı tanımlı bir bölen ayarlar. |
| [setTitleDeleted(boolean value)](#setTitleDeleted-boolean) |  |
| [setUnit(int value)](#setUnit-int) | Görüntü birimlerinin ölçekleme değerini önceden tanımlı değerlerden biri olarak ayarlar. |
### getCustomUnit() {#getCustomUnit}
```
public double getCustomUnit()
```


Değer eksenindeki görüntü birimlerini ölçeklemek için kullanıcı tanımlı bir bölen alır.

 **Remarks:** 

Bu özellik, MS Office 2016 yeni grafiklerinde desteklenmez. Varsayılan değer 1'dir.

Bu özelliği ayarlamak, [getUnit()](../../com.aspose.words/axisdisplayunit/\#getUnit) / [setUnit(int)](../../com.aspose.words/axisdisplayunit/\#setUnit-int) özelliğini [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM) olarak ayarlar.

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

**Returns:**
double - Değer eksenindeki görüntü birimlerini ölçeklemek için kullanıcı tanımlı bir bölen.
### getDefaultDisplayedFontSize() {#getDefaultDisplayedFontSize}
```
public double getDefaultDisplayedFontSize()
```




**Returns:**
double
### getDefaultFontSize() {#getDefaultFontSize}
```
public double getDefaultFontSize()
```




**Returns:**
double
### getDefaultTitleText() {#getDefaultTitleText}
```
public String getDefaultTitleText()
```




**Returns:**
java.lang.String
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Üst grafiği içeren belgeyi döndürür.

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

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The document containing the parent chart.
### getRelativeFontSize(int chartFontSize) {#getRelativeFontSize-int}
```
public int getRelativeFontSize(int chartFontSize)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartFontSize | int |  |

**Returns:**
int
### getStyleItem() {#getStyleItem}
```
public int getStyleItem()
```




**Returns:**
int
### getTitleDeleted() {#getTitleDeleted}
```
public boolean getTitleDeleted()
```




**Returns:**
boolean
### getTitlePosition() {#getTitlePosition}
```
public int getTitlePosition()
```




**Returns:**
int
### getUnit() {#getUnit}
```
public int getUnit()
```


Görüntü birimlerinin ölçekleme değerini önceden tanımlı değerlerden biri olarak alır.

 **Remarks:** 

Varsayılan değer [AxisBuiltInUnit.NONE](../../com.aspose.words/axisbuiltinunit/\#NONE)'dir. [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM) ve [AxisBuiltInUnit.PERCENTAGE](../../com.aspose.words/axisbuiltinunit/\#PERCENTAGE) değerleri bazı grafik türlerinde mevcut değildir; daha fazla bilgi için [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/) sayfasına bakın.

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

**Returns:**
int - Görüntü birimlerinin ölçekleme değeri, önceden tanımlı değerlerden biri olarak. Döndürülen değer, [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/) sabitlerinden biridir.
### isVisible() {#isVisible}
```
public boolean isVisible()
```




**Returns:**
boolean
### setCustomUnit(double value) {#setCustomUnit-double}
```
public void setCustomUnit(double value)
```


Değer eksenindeki görüntü birimlerini ölçeklemek için kullanıcı tanımlı bir bölen ayarlar.

 **Remarks:** 

Bu özellik, MS Office 2016 yeni grafiklerinde desteklenmez. Varsayılan değer 1'dir.

Bu özelliği ayarlamak, [getUnit()](../../com.aspose.words/axisdisplayunit/\#getUnit) / [setUnit(int)](../../com.aspose.words/axisdisplayunit/\#setUnit-int) özelliğini [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM) olarak ayarlar.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Değer eksenindeki görüntü birimlerini ölçeklemek için kullanıcı tanımlı bir bölen. |

### setTitleDeleted(boolean value) {#setTitleDeleted-boolean}
```
public void setTitleDeleted(boolean value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean |  |

### setUnit(int value) {#setUnit-int}
```
public void setUnit(int value)
```


Görüntü birimlerinin ölçekleme değerini önceden tanımlı değerlerden biri olarak ayarlar.

 **Remarks:** 

Varsayılan değer [AxisBuiltInUnit.NONE](../../com.aspose.words/axisbuiltinunit/\#NONE)'dir. [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM) ve [AxisBuiltInUnit.PERCENTAGE](../../com.aspose.words/axisbuiltinunit/\#PERCENTAGE) değerleri bazı grafik türlerinde mevcut değildir; daha fazla bilgi için [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/) sayfasına bakın.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Görüntü birimlerinin ölçekleme değeri, önceden tanımlı değerlerden biri olarak. Değer, [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/) sabitlerinden biri olmalıdır. |

