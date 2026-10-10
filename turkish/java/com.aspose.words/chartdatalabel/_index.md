---
title: "ChartDataLabel"
linktitle: "ChartDataLabel"
second_title: "Aspose.Words Java için"
description: "Java'da bir grafik noktasındaki veya eğri üzerindeki veri etiketini temsil eder."
type: docs
weight: 71
url: /tr/java/com.aspose.words/chartdatalabel/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartDataLabel implements Cloneable
```

Grafik noktasındaki veya eğri üzerindeki veri etiketini temsil eder.

Daha fazla bilgi için, [ Working with Charts ][Working with Charts] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bir seride, [ChartDataLabel](../../com.aspose.words/chartdatalabel/) nesnesi [ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection/) üyesidir. [ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection/) her nokta için bir [ChartDataLabel](../../com.aspose.words/chartdatalabel/) nesnesi içerir.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [clearFormat()](#clearFormat) | Bu veri etiketinin biçimini temizler. |
| [fetchSpecialDefaultRunPropertyValue(int key)](#fetchSpecialDefaultRunPropertyValue-int) |  |
| [generateItemText()](#generateItemText) |  |
| [getFont()](#getFont) | Bu veri etiketinin yazı tipi biçimlendirmesine erişim sağlar. |
| [getFormat()](#getFormat) | Veri etiketinin dolgu ve çizgi biçimlendirmesine erişim sağlar. |
| [getIndex()](#getIndex) | İçeren öğenin dizinini belirtir. |
| [getLeft()](#getLeft) | Veri etiketinin, grafiğin sol kenarından veya [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) özelliğiyle belirtilen konumdan puan cinsinden uzaklığını, [getLeftMode()](../../com.aspose.words/chartdatalabel/\#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/\#setLeftMode-int) özelliğinin değerine bağlı olarak alır. |
| [getLeftMode()](#getLeftMode) | [getLeft()](../../com.aspose.words/chartdatalabel/\#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/\#setLeft-double) özelliği değerinin yorumlama modunu alır: veri etiketinin konumunu grafiğin sol kenarından mı yoksa [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) özelliğiyle belirtilen konumdan mı ayarladığını. |
| [getNumberFormat()](#getNumberFormat) | Üst öğenin sayı biçimini döndürür. |
| [getOrientation()](#getOrientation) | Etiket metninin yönünü alır. |
| [getPosition()](#getPosition) | Veri etiketinin konumunu alır. |
| [getRelativePropertyValue(int key, Object value)](#getRelativePropertyValue-int-java.lang.Object) |  |
| [getRotation()](#getRotation) | Etiketin derece cinsinden dönüşünü alır. |
| [getSeparator()](#getSeparator) | Grafikteki veri etiketleri için kullanılan dize ayırıcıyı alır. |
| [getShapeType()](#getShapeType) |  |
| [getShowBubbleSize()](#getShowBubbleSize) | Bir grafikteki veri etiketleri için balon boyutunun görüntülenip görüntülenmeyeceğini belirtmeye izin verir. |
| [getShowCategoryName()](#getShowCategoryName) | Bir grafikteki veri etiketleri için kategori adının görüntülenip görüntülenmeyeceğini belirtmeye izin verir. |
| [getShowDataLabelsRange()](#getShowDataLabelsRange) | Veri etiketleri aralığından değerlerin veri etiketlerinde görüntülenip görüntülenmeyeceğini belirtmeye izin verir. |
| [getShowLeaderLines()](#getShowLeaderLines) | Veri etiketi lider çizgilerinin gösterilip gösterilmeyeceğini belirtmeye izin verir. |
| [getShowLegendKey()](#getShowLegendKey) | Bir grafikteki veri etiketleri için lejand anahtarının görüntülenip görüntülenmeyeceğini belirtmeye izin verir. |
| [getShowPercentage()](#getShowPercentage) | Bir grafikteki veri etiketleri için yüzde değerinin görüntülenip görüntülenmeyeceğini belirtmeye izin verir. |
| [getShowSeriesName()](#getShowSeriesName) | Bir grafikteki veri etiketleri için seri adının görüntülenme davranışını belirten bir Boolean alır. |
| [getShowValue()](#getShowValue) | Değerlerin veri etiketlerinde görüntülenip görüntülenmeyeceğini belirtmeye izin verir. |
| [getTop()](#getTop) | Veri etiketinin grafiğin üst kenarından veya [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int) özelliğiyle belirtilen konumdan puan cinsinden uzaklığını alır; bu, [getTopMode()](../../com.aspose.words/chartdatalabel/#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/#setTopMode-int) özelliğinin değerine bağlıdır. |
| [getTopMode()](#getTopMode) | Veri etiketinin konumunu grafiğin üst kenarından mı yoksa [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int) özelliğiyle belirtilen konumdan mı ayarladığını belirten [getTop()](../../com.aspose.words/chartdatalabel/#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/#setTop-double) özelliği değerinin yorumlama modunu alır. |
| [isFillSupported()](#isFillSupported) |  |
| [isFormatDefined()](#isFormatDefined) |  |
| [isHidden()](#isHidden) | Bu etiketin gizli olup olmadığını gösteren bir bayrağı alır/ayarlar. |
| [isHidden(boolean value)](#isHidden-boolean) | Bu etiketin gizli olup olmadığını gösteren bir bayrağı alır/ayarlar. |
| [isInherited()](#isInherited) |  |
| [isVisible()](#isVisible) | Bu veri etiketi görüntülenecek bir şeye sahipse  true  döndürür. |
| [materializeSpPr()](#materializeSpPr) |  |
| [setLeft(double value)](#setLeft-double) | Veri etiketinin grafiğin sol kenarından veya [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int) özelliğiyle belirtilen konumdan puan cinsinden uzaklığını ayarlar; bu, [getLeftMode()](../../com.aspose.words/chartdatalabel/#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/#setLeftMode-int) özelliğinin değerine bağlıdır. |
| [setLeftMode(int value)](#setLeftMode-int) | Veri etiketinin konumunu grafiğin sol kenarından mı yoksa [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int) özelliğiyle belirtilen konumdan mı ayarladığını belirten [getLeft()](../../com.aspose.words/chartdatalabel/#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/#setLeft-double) özelliği değerinin yorumlama modunu ayarlar. |
| [setOrientation(int value)](#setOrientation-int) | Etiket metninin yönünü ayarlar. |
| [setPosition(int value)](#setPosition-int) | Veri etiketinin konumunu ayarlar. |
| [setRotation(int value)](#setRotation-int) | Etiketin döndürülmesini derece cinsinden ayarlar. |
| [setSeparator(String value)](#setSeparator-java.lang.String) | Bir grafikteki veri etiketleri için kullanılan dize ayırıcıyı ayarlar. |
| [setShapeType(int value)](#setShapeType-int) |  |
| [setShowBubbleSize(boolean value)](#setShowBubbleSize-boolean) | Bir grafikteki veri etiketleri için balon boyutunun görüntülenip görüntülenmeyeceğini belirtmeye izin verir. |
| [setShowCategoryName(boolean value)](#setShowCategoryName-boolean) | Bir grafikteki veri etiketleri için kategori adının görüntülenip görüntülenmeyeceğini belirtmeye izin verir. |
| [setShowDataLabelsRange(boolean value)](#setShowDataLabelsRange-boolean) | Veri etiketleri aralığından değerlerin veri etiketlerinde görüntülenip görüntülenmeyeceğini belirtmeye izin verir. |
| [setShowLeaderLines(boolean value)](#setShowLeaderLines-boolean) | Veri etiketi lider çizgilerinin gösterilip gösterilmeyeceğini belirtmeye izin verir. |
| [setShowLegendKey(boolean value)](#setShowLegendKey-boolean) | Bir grafikteki veri etiketleri için lejand anahtarının görüntülenip görüntülenmeyeceğini belirtmeye izin verir. |
| [setShowPercentage(boolean value)](#setShowPercentage-boolean) | Bir grafikteki veri etiketleri için yüzde değerinin görüntülenip görüntülenmeyeceğini belirtmeye izin verir. |
| [setShowSeriesName(boolean value)](#setShowSeriesName-boolean) | Bir grafikteki veri etiketleri için seri adının görüntülenme davranışını belirten bir Boolean ayarlar. |
| [setShowValue(boolean value)](#setShowValue-boolean) | Değerlerin veri etiketlerinde görüntülenip görüntülenmeyeceğini belirtmeye izin verir. |
| [setTop(double value)](#setTop-double) | Veri etiketinin grafiğin üst kenarından veya [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int) özelliğiyle belirtilen konumdan puan cinsinden uzaklığını ayarlar; bu, [getTopMode()](../../com.aspose.words/chartdatalabel/#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/#setTopMode-int) özelliğinin değerine bağlıdır. |
| [setTopMode(int value)](#setTopMode-int) | Veri etiketinin konumunu grafiğin üst kenarından mı yoksa [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int) özelliğiyle belirtilen konumdan mı ayarladığını belirten [getTop()](../../com.aspose.words/chartdatalabel/#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/#setTop-double) özelliği değerinin yorumlama modunu ayarlar. |
### clearFormat() {#clearFormat}
```
public void clearFormat()
```


Bu veri etiketinin biçimini temizler. Özellikler, üst veri etiketi koleksiyonunda tanımlanan varsayılan değerlere ayarlanır.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

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


Bu veri etiketinin yazı tipi biçimlendirmesine erişim sağlar.

 **Examples:** 

Balon grafiklerinde 3B efektlerin nasıl kullanılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.BUBBLE_3_D, 500.0, 350.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());
 Assert.assertTrue(chart.getSeries().get(0).getBubble3D());

 // Apply a data label to each bubble that displays its diameter.
 for (int i = 0; i < 3; i++) {
     chart.getSeries().get(0).hasDataLabels(true);
     ChartDataLabel cdl = chart.getSeries().get(0).getDataLabels().get(i);
     chart.getSeries().get(0).getDataLabels().get(i).getFont().setSize(12.0);
     cdl.setShowBubbleSize(true);
 }

 doc.save(getArtifactsDir() + "Charts.Bubble3D.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getFormat() {#getFormat}
```
public ChartFormat getFormat()
```


Veri etiketinin dolgu ve çizgi biçimlendirmesine erişim sağlar.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
[ChartFormat](../../com.aspose.words/chartformat/) - The corresponding [ChartFormat](../../com.aspose.words/chartformat/) value.
### getIndex() {#getIndex}
```
public int getIndex()
```


İçeren öğenin dizinini belirtir. Bu dizin, ebeveynin çocuk koleksiyonundan bu öğenin hangi öğeye uygulanacağını belirler. Varsayılan değer 0.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
int - İlgili  int  değeri.
### getLeft() {#getLeft}
```
public double getLeft()
```


Veri etiketinin, grafiğin sol kenarından veya [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) özelliğiyle belirtilen konumdan puan cinsinden uzaklığını, [getLeftMode()](../../com.aspose.words/chartdatalabel/\#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/\#setLeftMode-int) özelliğinin değerine bağlı olarak alır.

 **Remarks:** 

Özelliğin değeri, grafik şekli yeniden boyutlandırılırsa orantılı olarak değişir.

Bu özellik, Word 2016 grafiğinde ayarlanamaz.

 **Examples:** 

Halka grafiğinin veri etiketlerinin halka dışına nasıl yerleştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Returns:**
double - Veri etiketinin, grafiğin sol kenarından veya [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) özelliğiyle belirtilen konumdan puan cinsinden uzaklığı, [getLeftMode()](../../com.aspose.words/chartdatalabel/\#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/\#setLeftMode-int) özelliğinin değerine bağlı olarak.
### getLeftMode() {#getLeftMode}
```
public int getLeftMode()
```


[getLeft()](../../com.aspose.words/chartdatalabel/\#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/\#setLeft-double) özelliği değerinin yorumlama modunu alır: veri etiketinin konumunu grafiğin sol kenarından mı yoksa [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) özelliğiyle belirtilen konumdan mı ayarladığını.

 **Remarks:** 

Bu özellik, Word 2016 grafiğinde ayarlanamaz.

 **Examples:** 

Halka grafiğinin veri etiketlerinin halka dışına nasıl yerleştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Returns:**
int - [getLeft()](../../com.aspose.words/chartdatalabel/\#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/\#setLeft-double) özelliği değerinin yorumlama modu: veri etiketinin konumunu grafiğin sol kenarından mı yoksa [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) özelliğiyle belirtilen konumdan mı ayarladığını belirler. Döndürülen değer, [ChartDataLabelLocationMode](../../com.aspose.words/chartdatalabellocationmode/) sabitlerinden biridir.
### getNumberFormat() {#getNumberFormat}
```
public ChartNumberFormat getNumberFormat()
```


Üst öğenin sayı biçimini döndürür.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
[ChartNumberFormat](../../com.aspose.words/chartnumberformat/) - Number format of the parent element.
### getOrientation() {#getOrientation}
```
public int getOrientation()
```


Etiket metninin yönünü alır.

 **Remarks:** 

Varsayılan değer [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL) dir.

 **Examples:** 

Veri etiketlerinin yönelim ve döndürülmesinin nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 ChartSeries series = shape.getChart().getSeries().get(0);
 ChartDataLabelCollection dataLabels = series.getDataLabels();

 // Show data labels.
 series.hasDataLabels(true);
 dataLabels.setShowValue(true);
 dataLabels.setShowCategoryName(true);

 // Define data label shape.
 dataLabels.getFormat().setShapeType(ChartShapeType.UP_ARROW);
 dataLabels.getFormat().getStroke().getFill().solid(Color.blue);

 // Set data label orientation and rotation for the entire series.
 dataLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 dataLabels.setRotation(-45);

 // Change orientation and rotation of the first data label.
 dataLabels.get(0).setOrientation(ShapeTextOrientation.HORIZONTAL);
 dataLabels.get(0).setRotation(45);

 doc.save(getArtifactsDir() + "Charts.LabelOrientationRotation.docx");
 
```

**Returns:**
int - Etiket metninin yönelimi. Döndürülen değer, [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/) sabitlerinden biridir.
### getPosition() {#getPosition}
```
public int getPosition()
```


Veri etiketinin konumunu alır.

 **Remarks:** 

Aşağıdaki grafik serisi türleri için veri etiketlerinin konumu ayarlanabilir:

\- [ChartSeriesType.BAR](../../com.aspose.words/chartseriestype/\#BAR), [ChartSeriesType.COLUMN](../../com.aspose.words/chartseriestype/\#COLUMN), [ChartSeriesType.HISTOGRAM](../../com.aspose.words/chartseriestype/\#HISTOGRAM), [ChartSeriesType.PARETO](../../com.aspose.words/chartseriestype/\#PARETO), [ChartSeriesType.WATERFALL](../../com.aspose.words/chartseriestype/\#WATERFALL); izin verilen değerler: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END) ve [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END);

\- [ChartSeriesType.BAR\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-STACKED), [ChartSeriesType.BAR\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-PERCENT-STACKED), [ChartSeriesType.COLUMN\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-STACKED), [ChartSeriesType.COLUMN\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-PERCENT-STACKED); izin verilen değerler: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE) ve [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END);

\- [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE), [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D), [ChartSeriesType.LINE](../../com.aspose.words/chartseriestype/\#LINE), [ChartSeriesType.LINE\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-STACKED), [ChartSeriesType.LINE\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-PERCENT-STACKED), [ChartSeriesType.SCATTER](../../com.aspose.words/chartseriestype/\#SCATTER), [ChartSeriesType.STOCK](../../com.aspose.words/chartseriestype/\#STOCK); izin verilen değerler: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) ve [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW);

\- [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D), [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR), [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE); izin verilen değerler: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END), [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END) ve [ChartDataLabelPosition.BEST\_FIT](../../com.aspose.words/chartdatalabelposition/\#BEST-FIT);

\- [ChartSeriesType.BOX\_AND\_WHISKER](../../com.aspose.words/chartseriestype/\#BOX-AND-WHISKER); izin verilen değerler: [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) ve [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW).

 **Examples:** 

Veri etiketinin konumunun nasıl ayarlanacağını gösterir.

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

**Returns:**
int - Veri etiketinin konumu. Döndürülen değer, [ChartDataLabelPosition](../../com.aspose.words/chartdatalabelposition/) sabitlerinden biridir.
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


Etiketin derece cinsinden dönüşünü alır.

 **Remarks:** 

Kabul edilebilir değer aralığı -180 ile 180 arasında, dahil. Varsayılan değer 0'dır.

Eğer [getOrientation()](../../com.aspose.words/chartdatalabel/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/chartdatalabel/\#setOrientation-int) değeri [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL) ise, mevcutsa etiket şekli, etiket metniyle birlikte döndürülür. Aksi takdirde yalnızca etiket metni döndürülür.

 **Examples:** 

Veri etiketlerinin yönelim ve döndürülmesinin nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 ChartSeries series = shape.getChart().getSeries().get(0);
 ChartDataLabelCollection dataLabels = series.getDataLabels();

 // Show data labels.
 series.hasDataLabels(true);
 dataLabels.setShowValue(true);
 dataLabels.setShowCategoryName(true);

 // Define data label shape.
 dataLabels.getFormat().setShapeType(ChartShapeType.UP_ARROW);
 dataLabels.getFormat().getStroke().getFill().solid(Color.blue);

 // Set data label orientation and rotation for the entire series.
 dataLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 dataLabels.setRotation(-45);

 // Change orientation and rotation of the first data label.
 dataLabels.get(0).setOrientation(ShapeTextOrientation.HORIZONTAL);
 dataLabels.get(0).setRotation(45);

 doc.save(getArtifactsDir() + "Charts.LabelOrientationRotation.docx");
 
```

**Returns:**
int - Etiketin derece cinsinden dönüşü.
### getSeparator() {#getSeparator}
```
public String getSeparator()
```


Bir grafikte veri etiketleri için kullanılan dize ayırıcıyı alır. Varsayılan olarak virgül kullanılır, yalnızca kategori adı ve yüzdeyi gösteren pasta grafiklerinde bunun yerine satır sonu kullanılır.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
java.lang.String - Bir grafikte veri etiketleri için kullanılan dize ayırıcı.
### getShapeType() {#getShapeType}
```
public int getShapeType()
```




**Returns:**
int
### getShowBubbleSize() {#getShowBubbleSize}
```
public boolean getShowBubbleSize()
```


Bir grafikte veri etiketleri için balon boyutunun gösterilip gösterilmeyeceğini belirtmeye izin verir. Yalnızca Balon grafiklerinde uygulanır. Varsayılan değer false.

 **Examples:** 

Balon grafiklerinde 3B efektlerin nasıl kullanılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.BUBBLE_3_D, 500.0, 350.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());
 Assert.assertTrue(chart.getSeries().get(0).getBubble3D());

 // Apply a data label to each bubble that displays its diameter.
 for (int i = 0; i < 3; i++) {
     chart.getSeries().get(0).hasDataLabels(true);
     ChartDataLabel cdl = chart.getSeries().get(0).getDataLabels().get(i);
     chart.getSeries().get(0).getDataLabels().get(i).getFont().setSize(12.0);
     cdl.setShowBubbleSize(true);
 }

 doc.save(getArtifactsDir() + "Charts.Bubble3D.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getShowCategoryName() {#getShowCategoryName}
```
public boolean getShowCategoryName()
```


Bir grafikte veri etiketleri için kategori adının gösterilip gösterilmeyeceğini belirtmeye izin verir. Varsayılan değer false.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getShowDataLabelsRange() {#getShowDataLabelsRange}
```
public boolean getShowDataLabelsRange()
```


Veri etiketleri aralığından değerlerin veri etiketlerinde gösterilip gösterilmeyeceğini belirtmeye izin verir. Varsayılan değer false.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getShowLeaderLines() {#getShowLeaderLines}
```
public boolean getShowLeaderLines()
```


Veri etiketi lider çizgilerinin gösterilip gösterilmeyeceğini belirtmeye izin verir. Varsayılan değer false.

 **Remarks:** 

Yalnızca Pasta grafiklerine uygulanır. Lider çizgiler, bir veri etiketi ile ona karşılık gelen veri noktası arasında görsel bir bağlantı oluşturur.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getShowLegendKey() {#getShowLegendKey}
```
public boolean getShowLegendKey()
```


Bir grafikte veri etiketleri için lejand anahtarının gösterilip gösterilmeyeceğini belirtmeye izin verir. Varsayılan değer false.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getShowPercentage() {#getShowPercentage}
```
public boolean getShowPercentage()
```


Bir grafikte veri etiketleri için yüzde değerinin gösterilip gösterilmeyeceğini belirtmeye izin verir. Varsayılan değer false.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getShowSeriesName() {#getShowSeriesName}
```
public boolean getShowSeriesName()
```


Bir grafikte veri etiketleri için seri adının gösterim davranışını belirten bir Boolean alır. seri adını göstermek için true; gizlemek için false. Varsayılan olarak false.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
boolean - Bir grafikte veri etiketleri için seri adının gösterim davranışını belirten bir Boolean.
### getShowValue() {#getShowValue}
```
public boolean getShowValue()
```


Veri etiketlerinde değerlerin gösterilip gösterilmeyeceğini belirtmeye izin verir. Varsayılan değer false.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getTop() {#getTop}
```
public double getTop()
```


Veri etiketinin grafiğin üst kenarından veya [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int) özelliğiyle belirtilen konumdan puan cinsinden uzaklığını alır; bu, [getTopMode()](../../com.aspose.words/chartdatalabel/#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/#setTopMode-int) özelliğinin değerine bağlıdır.

 **Remarks:** 

Özelliğin değeri, grafik şekli yeniden boyutlandırılırsa orantılı olarak değişir.

Bu özellik, Word 2016 grafiğinde ayarlanamaz.

 **Examples:** 

Halka grafiğinin veri etiketlerinin halka dışına nasıl yerleştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Returns:**
double - Veri etiketinin, grafiğin üst kenarından veya [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) özelliğiyle belirtilen konumdan puan cinsinden uzaklığı, [getTopMode()](../../com.aspose.words/chartdatalabel/\#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/\#setTopMode-int) özelliğinin değerine bağlı olarak.
### getTopMode() {#getTopMode}
```
public int getTopMode()
```


Veri etiketinin konumunu grafiğin üst kenarından mı yoksa [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int) özelliğiyle belirtilen konumdan mı ayarladığını belirten [getTop()](../../com.aspose.words/chartdatalabel/#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/#setTop-double) özelliği değerinin yorumlama modunu alır.

 **Remarks:** 

Bu özellik, Word 2016 grafiğinde ayarlanamaz.

 **Examples:** 

Halka grafiğinin veri etiketlerinin halka dışına nasıl yerleştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Returns:**
int - [getTop()](../../com.aspose.words/chartdatalabel/\#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/\#setTop-double) özelliğinin değerinin yorumlama modu: veri etiketinin konumunu grafiğin üst kenarından mı yoksa [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) özelliğiyle belirtilen konumdan mı ayarladığını belirler. Döndürülen değer, [ChartDataLabelLocationMode](../../com.aspose.words/chartdatalabellocationmode/) sabitlerinden biridir.
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
### isHidden() {#isHidden}
```
public boolean isHidden()
```


Bu etiketin gizli olup olmadığını gösteren bayrağı alır/ayar. Varsayılan değer false.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### isHidden(boolean value) {#isHidden-boolean}
```
public void isHidden(boolean value)
```


Bu etiketin gizli olup olmadığını gösteren bayrağı alır/ayar. Varsayılan değer false.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### isInherited() {#isInherited}
```
public boolean isInherited()
```




**Returns:**
boolean
### isVisible() {#isVisible}
```
public boolean isVisible()
```


Bu veri etiketi görüntülenecek bir şeye sahipse  true  döndürür.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
boolean - bu veri etiketi görüntülenecek bir şey içeriyorsa true.
### materializeSpPr() {#materializeSpPr}
```
public void materializeSpPr()
```




### setLeft(double value) {#setLeft-double}
```
public void setLeft(double value)
```


Veri etiketinin grafiğin sol kenarından veya [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int) özelliğiyle belirtilen konumdan puan cinsinden uzaklığını ayarlar; bu, [getLeftMode()](../../com.aspose.words/chartdatalabel/#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/#setLeftMode-int) özelliğinin değerine bağlıdır.

 **Remarks:** 

Özelliğin değeri, grafik şekli yeniden boyutlandırılırsa orantılı olarak değişir.

Bu özellik, Word 2016 grafiğinde ayarlanamaz.

 **Examples:** 

Halka grafiğinin veri etiketlerinin halka dışına nasıl yerleştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | double | Veri etiketinin, grafiğin sol kenarından veya [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) özelliğiyle belirtilen konumdan, [getLeftMode()](../../com.aspose.words/chartdatalabel/\#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/\#setLeftMode-int) özelliğinin değerine bağlı olarak, puan cinsinden uzaklığı. |

### setLeftMode(int value) {#setLeftMode-int}
```
public void setLeftMode(int value)
```


Veri etiketinin konumunu grafiğin sol kenarından mı yoksa [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int) özelliğiyle belirtilen konumdan mı ayarladığını belirten [getLeft()](../../com.aspose.words/chartdatalabel/#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/#setLeft-double) özelliği değerinin yorumlama modunu ayarlar.

 **Remarks:** 

Bu özellik, Word 2016 grafiğinde ayarlanamaz.

 **Examples:** 

Halka grafiğinin veri etiketlerinin halka dışına nasıl yerleştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | int - [getLeft()](../../com.aspose.words/chartdatalabel/\#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/\#setLeft-double) özelliğinin değerinin yorumlama modu: veri etiketinin konumunu grafiğin sol kenarından mı yoksa [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) özelliğiyle belirtilen konumdan mı ayarladığını belirler. Değer, [ChartDataLabelLocationMode](../../com.aspose.words/chartdatalabellocationmode/) sabitlerinden biri olmalıdır. |

### setOrientation(int value) {#setOrientation-int}
```
public void setOrientation(int value)
```


Etiket metninin yönünü ayarlar.

 **Remarks:** 

Varsayılan değer [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL) dir.

 **Examples:** 

Veri etiketlerinin yönelim ve döndürülmesinin nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 ChartSeries series = shape.getChart().getSeries().get(0);
 ChartDataLabelCollection dataLabels = series.getDataLabels();

 // Show data labels.
 series.hasDataLabels(true);
 dataLabels.setShowValue(true);
 dataLabels.setShowCategoryName(true);

 // Define data label shape.
 dataLabels.getFormat().setShapeType(ChartShapeType.UP_ARROW);
 dataLabels.getFormat().getStroke().getFill().solid(Color.blue);

 // Set data label orientation and rotation for the entire series.
 dataLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 dataLabels.setRotation(-45);

 // Change orientation and rotation of the first data label.
 dataLabels.get(0).setOrientation(ShapeTextOrientation.HORIZONTAL);
 dataLabels.get(0).setRotation(45);

 doc.save(getArtifactsDir() + "Charts.LabelOrientationRotation.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Etiket metninin yönelimi. Değer, [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/) sabitlerinden biri olmalıdır. |

### setPosition(int value) {#setPosition-int}
```
public void setPosition(int value)
```


Veri etiketinin konumunu ayarlar.

 **Remarks:** 

Aşağıdaki grafik serisi türleri için veri etiketlerinin konumu ayarlanabilir:

\- [ChartSeriesType.BAR](../../com.aspose.words/chartseriestype/\#BAR), [ChartSeriesType.COLUMN](../../com.aspose.words/chartseriestype/\#COLUMN), [ChartSeriesType.HISTOGRAM](../../com.aspose.words/chartseriestype/\#HISTOGRAM), [ChartSeriesType.PARETO](../../com.aspose.words/chartseriestype/\#PARETO), [ChartSeriesType.WATERFALL](../../com.aspose.words/chartseriestype/\#WATERFALL); izin verilen değerler: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END) ve [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END);

\- [ChartSeriesType.BAR\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-STACKED), [ChartSeriesType.BAR\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-PERCENT-STACKED), [ChartSeriesType.COLUMN\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-STACKED), [ChartSeriesType.COLUMN\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-PERCENT-STACKED); izin verilen değerler: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE) ve [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END);

\- [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE), [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D), [ChartSeriesType.LINE](../../com.aspose.words/chartseriestype/\#LINE), [ChartSeriesType.LINE\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-STACKED), [ChartSeriesType.LINE\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-PERCENT-STACKED), [ChartSeriesType.SCATTER](../../com.aspose.words/chartseriestype/\#SCATTER), [ChartSeriesType.STOCK](../../com.aspose.words/chartseriestype/\#STOCK); izin verilen değerler: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) ve [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW);

\- [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D), [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR), [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE); izin verilen değerler: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END), [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END) ve [ChartDataLabelPosition.BEST\_FIT](../../com.aspose.words/chartdatalabelposition/\#BEST-FIT);

\- [ChartSeriesType.BOX\_AND\_WHISKER](../../com.aspose.words/chartseriestype/\#BOX-AND-WHISKER); izin verilen değerler: [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) ve [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW).

 **Examples:** 

Veri etiketinin konumunun nasıl ayarlanacağını gösterir.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Veri etiketinin konumu. Değer, [ChartDataLabelPosition](../../com.aspose.words/chartdatalabelposition/) sabitlerinden biri olmalıdır. |

### setRotation(int value) {#setRotation-int}
```
public void setRotation(int value)
```


Etiketin döndürülmesini derece cinsinden ayarlar.

 **Remarks:** 

Kabul edilebilir değer aralığı -180 ile 180 arasında, dahil. Varsayılan değer 0'dır.

Eğer [getOrientation()](../../com.aspose.words/chartdatalabel/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/chartdatalabel/\#setOrientation-int) değeri [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL) ise, mevcutsa etiket şekli, etiket metniyle birlikte döndürülür. Aksi takdirde yalnızca etiket metni döndürülür.

 **Examples:** 

Veri etiketlerinin yönelim ve döndürülmesinin nasıl değiştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 ChartSeries series = shape.getChart().getSeries().get(0);
 ChartDataLabelCollection dataLabels = series.getDataLabels();

 // Show data labels.
 series.hasDataLabels(true);
 dataLabels.setShowValue(true);
 dataLabels.setShowCategoryName(true);

 // Define data label shape.
 dataLabels.getFormat().setShapeType(ChartShapeType.UP_ARROW);
 dataLabels.getFormat().getStroke().getFill().solid(Color.blue);

 // Set data label orientation and rotation for the entire series.
 dataLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 dataLabels.setRotation(-45);

 // Change orientation and rotation of the first data label.
 dataLabels.get(0).setOrientation(ShapeTextOrientation.HORIZONTAL);
 dataLabels.get(0).setRotation(45);

 doc.save(getArtifactsDir() + "Charts.LabelOrientationRotation.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Etiketin derece cinsinden dönüşü. |

### setSeparator(String value) {#setSeparator-java.lang.String}
```
public void setSeparator(String value)
```


Bir grafikteki veri etiketleri için kullanılan dize ayırıcıyı ayarlar. Varsayılan olarak virgül kullanılır; yalnızca kategori adı ve yüzdeyi gösteren pasta grafiklerinde bunun yerine satır sonu kullanılır.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Bir grafikteki veri etiketleri için kullanılan dize ayırıcı. |

### setShapeType(int value) {#setShapeType-int}
```
public void setShapeType(int value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int |  |

### setShowBubbleSize(boolean value) {#setShowBubbleSize-boolean}
```
public void setShowBubbleSize(boolean value)
```


Bir grafikte veri etiketleri için balon boyutunun gösterilip gösterilmeyeceğini belirtmeye izin verir. Yalnızca Balon grafiklerinde uygulanır. Varsayılan değer false.

 **Examples:** 

Balon grafiklerinde 3B efektlerin nasıl kullanılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.BUBBLE_3_D, 500.0, 350.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());
 Assert.assertTrue(chart.getSeries().get(0).getBubble3D());

 // Apply a data label to each bubble that displays its diameter.
 for (int i = 0; i < 3; i++) {
     chart.getSeries().get(0).hasDataLabels(true);
     ChartDataLabel cdl = chart.getSeries().get(0).getDataLabels().get(i);
     chart.getSeries().get(0).getDataLabels().get(i).getFont().setSize(12.0);
     cdl.setShowBubbleSize(true);
 }

 doc.save(getArtifactsDir() + "Charts.Bubble3D.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setShowCategoryName(boolean value) {#setShowCategoryName-boolean}
```
public void setShowCategoryName(boolean value)
```


Bir grafikte veri etiketleri için kategori adının gösterilip gösterilmeyeceğini belirtmeye izin verir. Varsayılan değer false.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setShowDataLabelsRange(boolean value) {#setShowDataLabelsRange-boolean}
```
public void setShowDataLabelsRange(boolean value)
```


Veri etiketleri aralığından değerlerin veri etiketlerinde gösterilip gösterilmeyeceğini belirtmeye izin verir. Varsayılan değer false.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setShowLeaderLines(boolean value) {#setShowLeaderLines-boolean}
```
public void setShowLeaderLines(boolean value)
```


Veri etiketi lider çizgilerinin gösterilip gösterilmeyeceğini belirtmeye izin verir. Varsayılan değer false.

 **Remarks:** 

Yalnızca Pasta grafiklerine uygulanır. Lider çizgiler, bir veri etiketi ile ona karşılık gelen veri noktası arasında görsel bir bağlantı oluşturur.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setShowLegendKey(boolean value) {#setShowLegendKey-boolean}
```
public void setShowLegendKey(boolean value)
```


Bir grafikte veri etiketleri için lejand anahtarının gösterilip gösterilmeyeceğini belirtmeye izin verir. Varsayılan değer false.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setShowPercentage(boolean value) {#setShowPercentage-boolean}
```
public void setShowPercentage(boolean value)
```


Bir grafikte veri etiketleri için yüzde değerinin gösterilip gösterilmeyeceğini belirtmeye izin verir. Varsayılan değer false.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setShowSeriesName(boolean value) {#setShowSeriesName-boolean}
```
public void setShowSeriesName(boolean value)
```


Bir grafikteki veri etiketleri için seri adının gösterim davranışını belirten bir Boolean ayarlar. true seri adını gösterir; false gizler. Varsayılan olarak false.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Bir grafikteki veri etiketleri için seri adının gösterim davranışını belirten bir Boolean. |

### setShowValue(boolean value) {#setShowValue-boolean}
```
public void setShowValue(boolean value)
```


Veri etiketlerinde değerlerin gösterilip gösterilmeyeceğini belirtmeye izin verir. Varsayılan değer false.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setTop(double value) {#setTop-double}
```
public void setTop(double value)
```


Veri etiketinin grafiğin üst kenarından veya [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int) özelliğiyle belirtilen konumdan puan cinsinden uzaklığını ayarlar; bu, [getTopMode()](../../com.aspose.words/chartdatalabel/#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/#setTopMode-int) özelliğinin değerine bağlıdır.

 **Remarks:** 

Özelliğin değeri, grafik şekli yeniden boyutlandırılırsa orantılı olarak değişir.

Bu özellik, Word 2016 grafiğinde ayarlanamaz.

 **Examples:** 

Halka grafiğinin veri etiketlerinin halka dışına nasıl yerleştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | double | Veri etiketinin, grafiğin üst kenarından veya [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) özelliğiyle belirtilen konumdan, [getTopMode()](../../com.aspose.words/chartdatalabel/\#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/\#setTopMode-int) özelliğinin değerine bağlı olarak, puan cinsinden uzaklığı. |

### setTopMode(int value) {#setTopMode-int}
```
public void setTopMode(int value)
```


Veri etiketinin konumunu grafiğin üst kenarından mı yoksa [getPosition()](../../com.aspose.words/chartdatalabel/#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/#setPosition-int) özelliğiyle belirtilen konumdan mı ayarladığını belirten [getTop()](../../com.aspose.words/chartdatalabel/#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/#setTop-double) özelliği değerinin yorumlama modunu ayarlar.

 **Remarks:** 

Bu özellik, Word 2016 grafiğinde ayarlanamaz.

 **Examples:** 

Halka grafiğinin veri etiketlerinin halka dışına nasıl yerleştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | int - [getTop()](../../com.aspose.words/chartdatalabel/\#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/\#setTop-double) özelliğinin değerinin yorumlama modu: veri etiketinin konumunu grafiğin üst kenarından mı yoksa [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) özelliğiyle belirtilen konumdan mı ayarladığını belirler. Değer, [ChartDataLabelLocationMode](../../com.aspose.words/chartdatalabellocationmode/) sabitlerinden biri olmalıdır. |

