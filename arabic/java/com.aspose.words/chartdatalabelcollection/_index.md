---
title: "ChartDataLabelCollection"
linktitle: "ChartDataLabelCollection"
second_title: "Aspose.Words لـ Java"
description: "يمثل مجموعة من ChartDataLabel في Java."
type: docs
weight: 72
url: /ar/java/com.aspose.words/chartdatalabelcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartDataLabelCollection implements Iterable
```

يمثل مجموعة من [ChartDataLabel](../../com.aspose.words/chartdatalabel/).

للتعرف على المزيد، زر مقالة توثيق [ Working with Charts ][Working with Charts].

 **Examples:** 

يوضح كيفية تطبيق التسميات على نقاط البيانات في مخطط خطي.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [clearFormat()](#clearFormat) | يمسح تنسيق جميع [ChartDataLabel](../../com.aspose.words/chartdatalabel/) في هذه المجموعة. |
| [get(int index)](#get-int) | يعيد [ChartDataLabel](../../com.aspose.words/chartdatalabel/) للفهرس المحدد. |
| [getCount()](#getCount) | يعيد عدد [ChartDataLabel](../../com.aspose.words/chartdatalabel/) في هذه المجموعة. |
| [getFont()](#getFont) | يوفر الوصول إلى تنسيق الخط لتسميات البيانات للسلسلة بأكملها. |
| [getFormat()](#getFormat) | يوفر الوصول إلى تنسيق التعبئة والخط لتسميات البيانات. |
| [getNumberFormat()](#getNumberFormat) | يحصل على كائن [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) يتيح تعيين تنسيق الأرقام لتسميات البيانات للسلسلة بأكملها. |
| [getOrientation()](#getOrientation) | يحصل على اتجاه النص لتسميات البيانات للسلسلة بأكملها. |
| [getPosition()](#getPosition) | يحصل على موضع تسميات البيانات. |
| [getRotation()](#getRotation) | يحصل على دوران تسميات البيانات للسلسلة بأكملها بالدرجات. |
| [getSeparator()](#getSeparator) | يحصل على فاصل السلسلة المستخدم لتسميات البيانات للسلسلة بأكملها. |
| [getShapeType()](#getShapeType) |  |
| [getShowBubbleSize()](#getShowBubbleSize) | يسمح بتحديد ما إذا كان حجم الفقاعات سيُعرض لتسميات البيانات للسلسلة بأكملها. |
| [getShowCategoryName()](#getShowCategoryName) | يسمح بتحديد ما إذا كان اسم الفئة سيُعرض لتسميات البيانات للسلسلة بأكملها. |
| [getShowDataLabelsRange()](#getShowDataLabelsRange) | يسمح بتحديد ما إذا كانت القيم من نطاق تسميات البيانات ستُعرض في تسميات البيانات للسلسلة بأكملها. |
| [getShowLeaderLines()](#getShowLeaderLines) | يسمح بتحديد ما إذا كانت خطوط ربط تسميات البيانات تحتاج إلى العرض لتسميات البيانات للسلسلة بأكملها. |
| [getShowLegendKey()](#getShowLegendKey) | يسمح بتحديد ما إذا كان مفتاح الوسيلة سيُعرض لتسميات البيانات للسلسلة بأكملها. |
| [getShowPercentage()](#getShowPercentage) | يسمح بتحديد ما إذا كانت القيمة النسبية ستُعرض لتسميات البيانات للسلسلة بأكملها. |
| [getShowSeriesName()](#getShowSeriesName) | يحصل على قيمة منطقية لتحديد سلوك عرض اسم السلسلة لتسميات البيانات للسلسلة بأكملها. |
| [getShowValue()](#getShowValue) | يسمح بتحديد ما إذا كانت القيم ستُعرض في تسميات البيانات للسلسلة بأكملها. |
| [isFillSupported()](#isFillSupported) |  |
| [isFormatDefined()](#isFormatDefined) |  |
| [isInherited()](#isInherited) |  |
| [iterator()](#iterator) | يرجع كائن عداد. |
| [materializeSpPr()](#materializeSpPr) |  |
| [setOrientation(int value)](#setOrientation-int) | يضبط اتجاه النص لتسميات البيانات للسلسلة بأكملها. |
| [setPosition(int value)](#setPosition-int) | يضبط موضع تسميات البيانات. |
| [setRotation(int value)](#setRotation-int) | يضبط دوران تسميات البيانات للسلسلة بأكملها بالدرجات. |
| [setSeparator(String value)](#setSeparator-java.lang.String) | يضبط فاصل السلسلة النصية المستخدم لتسميات البيانات للسلسلة بأكملها. |
| [setShapeType(int value)](#setShapeType-int) |  |
| [setShowBubbleSize(boolean value)](#setShowBubbleSize-boolean) | يسمح بتحديد ما إذا كان حجم الفقاعات سيُعرض لتسميات البيانات للسلسلة بأكملها. |
| [setShowCategoryName(boolean value)](#setShowCategoryName-boolean) | يسمح بتحديد ما إذا كان اسم الفئة سيُعرض لتسميات البيانات للسلسلة بأكملها. |
| [setShowDataLabelsRange(boolean value)](#setShowDataLabelsRange-boolean) | يسمح بتحديد ما إذا كانت القيم من نطاق تسميات البيانات ستُعرض في تسميات البيانات للسلسلة بأكملها. |
| [setShowLeaderLines(boolean value)](#setShowLeaderLines-boolean) | يسمح بتحديد ما إذا كانت خطوط ربط تسميات البيانات تحتاج إلى العرض لتسميات البيانات للسلسلة بأكملها. |
| [setShowLegendKey(boolean value)](#setShowLegendKey-boolean) | يسمح بتحديد ما إذا كان مفتاح الوسيلة سيُعرض لتسميات البيانات للسلسلة بأكملها. |
| [setShowPercentage(boolean value)](#setShowPercentage-boolean) | يسمح بتحديد ما إذا كانت القيمة النسبية ستُعرض لتسميات البيانات للسلسلة بأكملها. |
| [setShowSeriesName(boolean value)](#setShowSeriesName-boolean) | يضبط قيمة منطقية لتحديد سلوك عرض اسم السلسلة لتسميات البيانات للسلسلة بأكملها. |
| [setShowValue(boolean value)](#setShowValue-boolean) | يسمح بتحديد ما إذا كانت القيم ستُعرض في تسميات البيانات للسلسلة بأكملها. |
### clearFormat() {#clearFormat}
```
public void clearFormat()
```


يمسح تنسيق جميع [ChartDataLabel](../../com.aspose.words/chartdatalabel/) في هذه المجموعة.

 **Examples:** 

يوضح كيفية تطبيق التسميات على نقاط البيانات في مخطط خطي.

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

### get(int index) {#get-int}
```
public ChartDataLabel get(int index)
```


يعيد [ChartDataLabel](../../com.aspose.words/chartdatalabel/) للفهرس المحدد.

 **Examples:** 

يوضح كيفية تطبيق التسميات على نقاط البيانات في مخطط خطي.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int |  |

**Returns:**
[ChartDataLabel](../../com.aspose.words/chartdatalabel/) - [ChartDataLabel](../../com.aspose.words/chartdatalabel/) for the specified index.
### getCount() {#getCount}
```
public int getCount()
```


يعيد عدد [ChartDataLabel](../../com.aspose.words/chartdatalabel/) في هذه المجموعة.

 **Examples:** 

يوضح كيفية تطبيق التسميات على نقاط البيانات في مخطط خطي.

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
int - عدد [ChartDataLabel](../../com.aspose.words/chartdatalabel/) في هذه المجموعة.
### getFont() {#getFont}
```
public Font getFont()
```


يوفر الوصول إلى تنسيق الخط لتسميات البيانات للسلسلة بأكملها.

 **Remarks:** 

يمكن تجاوز القيمة المعرفة لهذا الخاصية لتسمية بيانات فردية باستخدام خاصية [ChartDataLabel.getFont()](../../com.aspose.words/chartdatalabel/\#getFont).

 **Examples:** 

يعرض كيفية تمكين وتكوين علامات البيانات لسلسلة مخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a line chart, then clear its demo data series to start with a clean chart,
 // and then set a title.
 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();
 chart.getSeries().clear();
 chart.getTitle().setText("Monthly sales report");

 // Insert a custom chart series with months as categories for the X-axis,
 // and respective decimal amounts for the Y-axis.
 ChartSeries series = chart.getSeries().add("Revenue",
         new String[]{"January", "February", "March"},
         new double[]{25.611d, 21.439d, 33.750d});

 // Enable data labels, and then apply a custom number format for values displayed in the data labels.
 // This format will treat displayed decimal values as millions of US Dollars.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.getNumberFormat().setFormatCode("\"US$\" #,##0.000\"M\"");
 dataLabels.getFont().setSize(12.0);

 doc.save(getArtifactsDir() + "Charts.DataLabelNumberFormat.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getFormat() {#getFormat}
```
public ChartFormat getFormat()
```


يوفر الوصول إلى تنسيق التعبئة والخط لتسميات البيانات.

 **Examples:** 

يظهر كيفية تعيين التعبئة، الحد وتنسيق التعليق لتسميات بيانات المخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 // Add new series.
 ChartSeries series = chart.getSeries().add("AW Series 1",
         new String[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
         new double[] { 100.0, 200.0, 300.0, 400.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowValue(true);

 // Format data labels as callouts.
 ChartFormat format = series.getDataLabels().getFormat();
 format.setShapeType(ChartShapeType.WEDGE_RECT_CALLOUT);
 format.getStroke().setColor(Color.lightGray);
 format.getFill().solid(Color.GREEN);
 series.getDataLabels().getFont().setColor(Color.YELLOW);

 // Change fill and stroke of an individual data label.
 ChartFormat labelFormat = series.getDataLabels().get(0).getFormat();
 labelFormat.getStroke().setColor(Color.BLUE);
 labelFormat.getFill().solid(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.FormatDataLables.docx");
 
```

**Returns:**
[ChartFormat](../../com.aspose.words/chartformat/) - The corresponding [ChartFormat](../../com.aspose.words/chartformat/) value.
### getNumberFormat() {#getNumberFormat}
```
public ChartNumberFormat getNumberFormat()
```


يحصل على كائن [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) يتيح تعيين تنسيق الأرقام لتسميات البيانات للسلسلة بأكملها.

 **Examples:** 

يعرض كيفية تمكين وتكوين علامات البيانات لسلسلة مخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a line chart, then clear its demo data series to start with a clean chart,
 // and then set a title.
 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();
 chart.getSeries().clear();
 chart.getTitle().setText("Monthly sales report");

 // Insert a custom chart series with months as categories for the X-axis,
 // and respective decimal amounts for the Y-axis.
 ChartSeries series = chart.getSeries().add("Revenue",
         new String[]{"January", "February", "March"},
         new double[]{25.611d, 21.439d, 33.750d});

 // Enable data labels, and then apply a custom number format for values displayed in the data labels.
 // This format will treat displayed decimal values as millions of US Dollars.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.getNumberFormat().setFormatCode("\"US$\" #,##0.000\"M\"");
 dataLabels.getFont().setSize(12.0);

 doc.save(getArtifactsDir() + "Charts.DataLabelNumberFormat.docx");
 
```

**Returns:**
[ChartNumberFormat](../../com.aspose.words/chartnumberformat/) - An [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) instance allowing to set number format for the data labels of the entire series.
### getOrientation() {#getOrientation}
```
public int getOrientation()
```


يحصل على اتجاه النص لتسميات البيانات للسلسلة بأكملها.

 **Remarks:** 

القيمة الافتراضية هي [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL).

 **Examples:** 

يوضح كيفية تغيير الاتجاه والدوران لتسميات البيانات.

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
int - اتجاه النص لتسميات البيانات للسلسلة بأكملها. القيمة المرجعة هي واحدة من ثوابت [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/).
### getPosition() {#getPosition}
```
public int getPosition()
```


يحصل على موضع تسميات البيانات.

 **Remarks:** 

يمكن ضبط الموضع لتسميات البيانات للأنواع التالية من سلاسل المخطط:

\- [ChartSeriesType.BAR](../../com.aspose.words/chartseriestype/\#BAR), [ChartSeriesType.COLUMN](../../com.aspose.words/chartseriestype/\#COLUMN), [ChartSeriesType.HISTOGRAM](../../com.aspose.words/chartseriestype/\#HISTOGRAM), [ChartSeriesType.PARETO](../../com.aspose.words/chartseriestype/\#PARETO), [ChartSeriesType.WATERFALL](../../com.aspose.words/chartseriestype/\#WATERFALL); القيم المسموح بها: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END) و [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END);

\- [ChartSeriesType.BAR\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-STACKED), [ChartSeriesType.BAR\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-PERCENT-STACKED), [ChartSeriesType.COLUMN\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-STACKED), [ChartSeriesType.COLUMN\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-PERCENT-STACKED); القيم المسموح بها: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE) و [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END);

\- [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE), [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D), [ChartSeriesType.LINE](../../com.aspose.words/chartseriestype/\#LINE), [ChartSeriesType.LINE\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-STACKED), [ChartSeriesType.LINE\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-PERCENT-STACKED), [ChartSeriesType.SCATTER](../../com.aspose.words/chartseriestype/\#SCATTER), [ChartSeriesType.STOCK](../../com.aspose.words/chartseriestype/\#STOCK); القيم المسموح بها: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) و [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW);

- [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D), [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR), [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE)؛ القيم المسموح بها: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END), [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END) و [ChartDataLabelPosition.BEST\_FIT](../../com.aspose.words/chartdatalabelposition/\#BEST-FIT)؛

- [ChartSeriesType.BOX\_AND\_WHISKER](../../com.aspose.words/chartseriestype/\#BOX-AND-WHISKER)؛ القيم المسموح بها: [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) و [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW).

 **Examples:** 

يوضح كيفية تعيين موضع تسمية البيانات.

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
int - موضع تسميات البيانات. القيمة المرجعة هي إحدى ثوابت [ChartDataLabelPosition](../../com.aspose.words/chartdatalabelposition/\#).
### getRotation() {#getRotation}
```
public int getRotation()
```


يحصل على دوران تسميات البيانات للسلسلة بأكملها بالدرجات.

 **Remarks:** 

نطاق القيم المقبولة هو من -180 إلى 180 شاملًا. القيمة الافتراضية هي 0.

إذا كانت قيمة [getOrientation()](../../com.aspose.words/chartdatalabelcollection/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/chartdatalabelcollection/\#setOrientation-int) هي [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL)، فإن أشكال التسمية، إذا وجدت، تُدوَّر مع نص التسمية. وإلا، يُدوَّر نص التسمية فقط.

 **Examples:** 

يوضح كيفية تغيير الاتجاه والدوران لتسميات البيانات.

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
int - دوران تسميات البيانات للسلسلة بأكملها بالدرجات.
### getSeparator() {#getSeparator}
```
public String getSeparator()
```


يحصل على الفاصل النصي المستخدم لتسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي الفاصلة، باستثناء المخططات الدائرية التي تُظهر فقط اسم الفئة والنسبة المئوية، حيث يُستَخدم فاصل سطر بدلاً من ذلك.

 **Remarks:** 

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getSeparator()](../../com.aspose.words/chartdatalabel/\#getSeparator) / [ChartDataLabel.setSeparator(java.lang.String)](../../com.aspose.words/chartdatalabel/\#setSeparator-java.lang.String).

 **Examples:** 

يوضح كيفية العمل مع تسميات البيانات في مخطط الفقاعات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

يوضح كيفية العمل مع تسميات البيانات في مخطط دائري.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Returns:**
java.lang.String - الفاصل النصي المستخدم لتسميات البيانات للسلسلة بأكملها.
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


يسمح بتحديد ما إذا كان يجب عرض حجم الفقاعة لتسميات البيانات للسلسلة بأكملها. ينطبق فقط على مخططات الفقاعات. القيمة الافتراضية هي false.

 **Remarks:** 

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getShowBubbleSize()](../../com.aspose.words/chartdatalabel/\#getShowBubbleSize) / [ChartDataLabel.setShowBubbleSize(boolean)](../../com.aspose.words/chartdatalabel/\#setShowBubbleSize-boolean).

 **Examples:** 

يوضح كيفية العمل مع تسميات البيانات في مخطط الفقاعات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getShowCategoryName() {#getShowCategoryName}
```
public boolean getShowCategoryName()
```


يسمح بتحديد ما إذا كان يجب عرض اسم الفئة لتسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي false.

 **Remarks:** 

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getShowCategoryName()](../../com.aspose.words/chartdatalabel/\#getShowCategoryName) / [ChartDataLabel.setShowCategoryName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowCategoryName-boolean).

 **Examples:** 

يوضح كيفية العمل مع تسميات البيانات في مخطط الفقاعات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getShowDataLabelsRange() {#getShowDataLabelsRange}
```
public boolean getShowDataLabelsRange()
```


يسمح بتحديد ما إذا كان يجب عرض القيم من نطاق تسميات البيانات في تسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي false.

 **Remarks:** 

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getShowDataLabelsRange()](../../com.aspose.words/chartdatalabel/\#getShowDataLabelsRange) / [ChartDataLabel.setShowDataLabelsRange(boolean)](../../com.aspose.words/chartdatalabel/\#setShowDataLabelsRange-boolean).

 **Examples:** 

يوضح كيفية تطبيق التسميات على نقاط البيانات في مخطط خطي.

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
boolean - القيمة المنطقية المقابلة.
### getShowLeaderLines() {#getShowLeaderLines}
```
public boolean getShowLeaderLines()
```


يسمح بتحديد ما إذا كان يجب إظهار خطوط القادة لتسميات البيانات لسلسلة البيانات بالكامل. القيمة الافتراضية هي false.

 **Remarks:** 

ينطبق على مخططات الفطيرة فقط. خطوط القادة تخلق اتصالًا بصريًا بين تسمية البيانات والنقطة البيانات المقابلة لها.

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getShowLeaderLines()](../../com.aspose.words/chartdatalabel/\#getShowLeaderLines) / [ChartDataLabel.setShowLeaderLines(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLeaderLines-boolean).

 **Examples:** 

يوضح كيفية العمل مع تسميات البيانات في مخطط دائري.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getShowLegendKey() {#getShowLegendKey}
```
public boolean getShowLegendKey()
```


يسمح بتحديد ما إذا كان مفتاح الوسيلة يجب عرضه لتسميات البيانات لسلسلة البيانات بالكامل. القيمة الافتراضية هي false.

 **Remarks:** 

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getShowLegendKey()](../../com.aspose.words/chartdatalabel/\#getShowLegendKey) / [ChartDataLabel.setShowLegendKey(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLegendKey-boolean).

 **Examples:** 

يوضح كيفية العمل مع تسميات البيانات في مخطط دائري.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getShowPercentage() {#getShowPercentage}
```
public boolean getShowPercentage()
```


يسمح بتحديد ما إذا كان يجب عرض قيمة النسبة المئوية لتسميات البيانات لسلسلة البيانات بالكامل. القيمة الافتراضية هي false. ينطبق فقط على مخططات الفطيرة.

 **Remarks:** 

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getShowPercentage()](../../com.aspose.words/chartdatalabel/\#getShowPercentage) / [ChartDataLabel.setShowPercentage(boolean)](../../com.aspose.words/chartdatalabel/\#setShowPercentage-boolean).

 **Examples:** 

يوضح كيفية العمل مع تسميات البيانات في مخطط دائري.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getShowSeriesName() {#getShowSeriesName}
```
public boolean getShowSeriesName()
```


يحصل على قيمة منطقية لتحديد سلوك عرض اسم السلسلة لتسميات البيانات لسلسلة البيانات بالكامل. true لعرض اسم السلسلة؛ false لإخفائه. بشكل افتراضي false.

 **Remarks:** 

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getShowSeriesName()](../../com.aspose.words/chartdatalabel/\#getShowSeriesName) / [ChartDataLabel.setShowSeriesName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowSeriesName-boolean).

 **Examples:** 

يوضح كيفية العمل مع تسميات البيانات في مخطط الفقاعات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Returns:**
boolean - قيمة منطقية لتحديد سلوك عرض اسم السلسلة لتسميات البيانات لسلسلة البيانات بالكامل.
### getShowValue() {#getShowValue}
```
public boolean getShowValue()
```


يسمح بتحديد ما إذا كان يجب عرض القيم في تسميات البيانات لسلسلة البيانات بالكامل. القيمة الافتراضية هي false.

 **Remarks:** 

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getShowValue()](../../com.aspose.words/chartdatalabel/\#getShowValue) / [ChartDataLabel.setShowValue(boolean)](../../com.aspose.words/chartdatalabel/\#setShowValue-boolean).

 **Examples:** 

يوضح كيفية العمل مع تسميات البيانات في مخطط دائري.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
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
### isInherited() {#isInherited}
```
public boolean isInherited()
```




**Returns:**
boolean
### iterator() {#iterator}
```
public Iterator iterator()
```


يرجع كائن عداد.

 **Examples:** 

يوضح كيفية تطبيق التسميات على نقاط البيانات في مخطط خطي.

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
java.util.Iterator
### materializeSpPr() {#materializeSpPr}
```
public void materializeSpPr()
```




### setOrientation(int value) {#setOrientation-int}
```
public void setOrientation(int value)
```


يضبط اتجاه النص لتسميات البيانات للسلسلة بأكملها.

 **Remarks:** 

القيمة الافتراضية هي [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL).

 **Examples:** 

يوضح كيفية تغيير الاتجاه والدوران لتسميات البيانات.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | اتجاه النص لتسميات البيانات لسلسلة البيانات بالكامل. يجب أن تكون القيمة واحدة من ثوابت [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/). |

### setPosition(int value) {#setPosition-int}
```
public void setPosition(int value)
```


يضبط موضع تسميات البيانات.

 **Remarks:** 

يمكن ضبط الموضع لتسميات البيانات للأنواع التالية من سلاسل المخطط:

\- [ChartSeriesType.BAR](../../com.aspose.words/chartseriestype/\#BAR), [ChartSeriesType.COLUMN](../../com.aspose.words/chartseriestype/\#COLUMN), [ChartSeriesType.HISTOGRAM](../../com.aspose.words/chartseriestype/\#HISTOGRAM), [ChartSeriesType.PARETO](../../com.aspose.words/chartseriestype/\#PARETO), [ChartSeriesType.WATERFALL](../../com.aspose.words/chartseriestype/\#WATERFALL); القيم المسموح بها: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END) و [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END);

\- [ChartSeriesType.BAR\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-STACKED), [ChartSeriesType.BAR\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-PERCENT-STACKED), [ChartSeriesType.COLUMN\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-STACKED), [ChartSeriesType.COLUMN\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-PERCENT-STACKED); القيم المسموح بها: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE) و [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END);

\- [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE), [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D), [ChartSeriesType.LINE](../../com.aspose.words/chartseriestype/\#LINE), [ChartSeriesType.LINE\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-STACKED), [ChartSeriesType.LINE\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-PERCENT-STACKED), [ChartSeriesType.SCATTER](../../com.aspose.words/chartseriestype/\#SCATTER), [ChartSeriesType.STOCK](../../com.aspose.words/chartseriestype/\#STOCK); القيم المسموح بها: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) و [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW);

- [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D), [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR), [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE)؛ القيم المسموح بها: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END), [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END) و [ChartDataLabelPosition.BEST\_FIT](../../com.aspose.words/chartdatalabelposition/\#BEST-FIT)؛

- [ChartSeriesType.BOX\_AND\_WHISKER](../../com.aspose.words/chartseriestype/\#BOX-AND-WHISKER)؛ القيم المسموح بها: [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) و [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW).

 **Examples:** 

يوضح كيفية تعيين موضع تسمية البيانات.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | موضع تسميات البيانات. يجب أن تكون القيمة واحدة من ثوابت [ChartDataLabelPosition](../../com.aspose.words/chartdatalabelposition/). |

### setRotation(int value) {#setRotation-int}
```
public void setRotation(int value)
```


يضبط دوران تسميات البيانات للسلسلة بأكملها بالدرجات.

 **Remarks:** 

نطاق القيم المقبولة هو من -180 إلى 180 شاملًا. القيمة الافتراضية هي 0.

إذا كانت قيمة [getOrientation()](../../com.aspose.words/chartdatalabelcollection/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/chartdatalabelcollection/\#setOrientation-int) هي [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL)، فإن أشكال التسمية، إذا وجدت، تُدوَّر مع نص التسمية. وإلا، يُدوَّر نص التسمية فقط.

 **Examples:** 

يوضح كيفية تغيير الاتجاه والدوران لتسميات البيانات.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | دوران تسميات البيانات لسلسلة البيانات بالكامل بالدرجات. |

### setSeparator(String value) {#setSeparator-java.lang.String}
```
public void setSeparator(String value)
```


يضبط الفاصل النصي المستخدم لتسميات البيانات لسلسلة البيانات بالكامل. الافتراضي هو الفاصلة، باستثناء مخططات الفطيرة التي تعرض فقط اسم الفئة والنسبة المئوية، حيث يُستخدم كسر السطر بدلاً من ذلك.

 **Remarks:** 

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getSeparator()](../../com.aspose.words/chartdatalabel/\#getSeparator) / [ChartDataLabel.setSeparator(java.lang.String)](../../com.aspose.words/chartdatalabel/\#setSeparator-java.lang.String).

 **Examples:** 

يوضح كيفية العمل مع تسميات البيانات في مخطط الفقاعات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

يوضح كيفية العمل مع تسميات البيانات في مخطط دائري.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | الفاصل النصي المستخدم لتسميات البيانات لسلسلة البيانات بالكامل. |

### setShapeType(int value) {#setShapeType-int}
```
public void setShapeType(int value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int |  |

### setShowBubbleSize(boolean value) {#setShowBubbleSize-boolean}
```
public void setShowBubbleSize(boolean value)
```


يسمح بتحديد ما إذا كان يجب عرض حجم الفقاعة لتسميات البيانات للسلسلة بأكملها. ينطبق فقط على مخططات الفقاعات. القيمة الافتراضية هي false.

 **Remarks:** 

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getShowBubbleSize()](../../com.aspose.words/chartdatalabel/\#getShowBubbleSize) / [ChartDataLabel.setShowBubbleSize(boolean)](../../com.aspose.words/chartdatalabel/\#setShowBubbleSize-boolean).

 **Examples:** 

يوضح كيفية العمل مع تسميات البيانات في مخطط الفقاعات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setShowCategoryName(boolean value) {#setShowCategoryName-boolean}
```
public void setShowCategoryName(boolean value)
```


يسمح بتحديد ما إذا كان يجب عرض اسم الفئة لتسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي false.

 **Remarks:** 

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getShowCategoryName()](../../com.aspose.words/chartdatalabel/\#getShowCategoryName) / [ChartDataLabel.setShowCategoryName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowCategoryName-boolean).

 **Examples:** 

يوضح كيفية العمل مع تسميات البيانات في مخطط الفقاعات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setShowDataLabelsRange(boolean value) {#setShowDataLabelsRange-boolean}
```
public void setShowDataLabelsRange(boolean value)
```


يسمح بتحديد ما إذا كان يجب عرض القيم من نطاق تسميات البيانات في تسميات البيانات للسلسلة بأكملها. القيمة الافتراضية هي false.

 **Remarks:** 

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getShowDataLabelsRange()](../../com.aspose.words/chartdatalabel/\#getShowDataLabelsRange) / [ChartDataLabel.setShowDataLabelsRange(boolean)](../../com.aspose.words/chartdatalabel/\#setShowDataLabelsRange-boolean).

 **Examples:** 

يوضح كيفية تطبيق التسميات على نقاط البيانات في مخطط خطي.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setShowLeaderLines(boolean value) {#setShowLeaderLines-boolean}
```
public void setShowLeaderLines(boolean value)
```


يسمح بتحديد ما إذا كان يجب إظهار خطوط القادة لتسميات البيانات لسلسلة البيانات بالكامل. القيمة الافتراضية هي false.

 **Remarks:** 

ينطبق على مخططات الفطيرة فقط. خطوط القادة تخلق اتصالًا بصريًا بين تسمية البيانات والنقطة البيانات المقابلة لها.

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getShowLeaderLines()](../../com.aspose.words/chartdatalabel/\#getShowLeaderLines) / [ChartDataLabel.setShowLeaderLines(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLeaderLines-boolean).

 **Examples:** 

يوضح كيفية العمل مع تسميات البيانات في مخطط دائري.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setShowLegendKey(boolean value) {#setShowLegendKey-boolean}
```
public void setShowLegendKey(boolean value)
```


يسمح بتحديد ما إذا كان مفتاح الوسيلة يجب عرضه لتسميات البيانات لسلسلة البيانات بالكامل. القيمة الافتراضية هي false.

 **Remarks:** 

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getShowLegendKey()](../../com.aspose.words/chartdatalabel/\#getShowLegendKey) / [ChartDataLabel.setShowLegendKey(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLegendKey-boolean).

 **Examples:** 

يوضح كيفية العمل مع تسميات البيانات في مخطط دائري.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setShowPercentage(boolean value) {#setShowPercentage-boolean}
```
public void setShowPercentage(boolean value)
```


يسمح بتحديد ما إذا كان يجب عرض قيمة النسبة المئوية لتسميات البيانات لسلسلة البيانات بالكامل. القيمة الافتراضية هي false. ينطبق فقط على مخططات الفطيرة.

 **Remarks:** 

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getShowPercentage()](../../com.aspose.words/chartdatalabel/\#getShowPercentage) / [ChartDataLabel.setShowPercentage(boolean)](../../com.aspose.words/chartdatalabel/\#setShowPercentage-boolean).

 **Examples:** 

يوضح كيفية العمل مع تسميات البيانات في مخطط دائري.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setShowSeriesName(boolean value) {#setShowSeriesName-boolean}
```
public void setShowSeriesName(boolean value)
```


يضبط قيمة منطقية لتحديد سلوك عرض اسم السلسلة لتسميات البيانات لسلسلة البيانات بالكامل. true لعرض اسم السلسلة؛ false لإخفائه. بشكل افتراضي false.

 **Remarks:** 

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getShowSeriesName()](../../com.aspose.words/chartdatalabel/\#getShowSeriesName) / [ChartDataLabel.setShowSeriesName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowSeriesName-boolean).

 **Examples:** 

يوضح كيفية العمل مع تسميات البيانات في مخطط الفقاعات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | قيمة منطقية لتحديد سلوك عرض اسم السلسلة لتسميات البيانات لسلسلة البيانات بالكامل. |

### setShowValue(boolean value) {#setShowValue-boolean}
```
public void setShowValue(boolean value)
```


يسمح بتحديد ما إذا كان يجب عرض القيم في تسميات البيانات لسلسلة البيانات بالكامل. القيمة الافتراضية هي false.

 **Remarks:** 

القيمة المحددة لهذا الخاصية يمكن تجاوزها لتسمية بيانات فردية باستخدام الخاصية [ChartDataLabel.getShowValue()](../../com.aspose.words/chartdatalabel/\#getShowValue) / [ChartDataLabel.setShowValue(boolean)](../../com.aspose.words/chartdatalabel/\#setShowValue-boolean).

 **Examples:** 

يوضح كيفية العمل مع تسميات البيانات في مخطط دائري.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

