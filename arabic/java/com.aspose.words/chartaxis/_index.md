---
title: "ChartAxis"
linktitle: "ChartAxis"
second_title: "Aspose.Words لـ Java"
description: "يمثل خيارات المحور للمخطط في Java."
type: docs
weight: 67
url: /ar/java/com.aspose.words/chartaxis/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartAxis implements Cloneable
```

يمثل خيارات المحور للمخطط.

للتعرف على المزيد، زر مقالة توثيق [ Working with Charts ][Working with Charts].

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getAxisBetweenCategories()](#getAxisBetweenCategories) | يحصل على علم يشير إلى ما إذا كان محور القيمة يعبر محور الفئة بين الفئات. |
| [getBaseTimeUnit()](#getBaseTimeUnit) | يحصل على أصغر وحدة زمنية ممثلة على محور الفئة الزمنية. |
| [getCategoryType()](#getCategoryType) | يحصل على نوع محور الفئة. |
| [getCrosses()](#getCrosses) | يحدد كيفية عبور هذا المحور للمحور المتعامد. |
| [getCrossesAt()](#getCrossesAt) | يحدد أين على المحور المتعامد يعبر المحور. |
| [getDefaultDisplayedFontSize()](#getDefaultDisplayedFontSize) |  |
| [getDefaultFontSize()](#getDefaultFontSize) |  |
| [getDefaultTitleText()](#getDefaultTitleText) |  |
| [getDisplayUnit()](#getDisplayUnit) | يحدد قيمة التحجيم لوحدات العرض لمحور القيم. |
| [getDocument()](#getDocument) | يرجع المستند الذي يحتوي على المخطط الأصلي. |
| [getFormat()](#getFormat) | يوفر الوصول إلى تنسيق الخط للمحور وتعبئة تسميات العلامات. |
| [getHidden()](#getHidden) | يحصل على علم يشير إلى ما إذا كان هذا المحور مخفيًا أم لا. |
| [getMajorTickMark()](#getMajorTickMark) | يحصل على العلامات الرئيسية. |
| [getMajorUnit()](#getMajorUnit) | يحصل على المسافة بين العلامات الرئيسية. |
| [getMajorUnitIsAuto()](#getMajorUnitIsAuto) | يحصل على علم يشير إلى ما إذا كان يجب استخدام المسافة الافتراضية بين العلامات الرئيسية. |
| [getMajorUnitScale()](#getMajorUnitScale) | يحصل على قيمة المقياس للعلامات الرئيسية على محور الفئة الزمنية. |
| [getMinorTickMark()](#getMinorTickMark) | يحصل على العلامات الفرعية للمحور. |
| [getMinorUnit()](#getMinorUnit) | يحصل على المسافة بين العلامات الفرعية. |
| [getMinorUnitIsAuto()](#getMinorUnitIsAuto) | يحصل على علم يشير إلى ما إذا كان يجب استخدام المسافة الافتراضية بين العلامات الفرعية. |
| [getMinorUnitScale()](#getMinorUnitScale) | يحصل على قيمة المقياس للعلامات الفرعية على محور الفئة الزمنية. |
| [getNumberFormat()](#getNumberFormat) | يعيد كائن [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) الذي يتيح تعريف تنسيقات الأرقام للمحور. |
| [getRelativeFontSize(int chartFontSize)](#getRelativeFontSize-int) |  |
| [getReverseOrder()](#getReverseOrder) | يحصل على علم يشير إلى ما إذا كان يجب عرض قيم المحور بترتيب عكسي، أي. |
| [getScaling()](#getScaling) | يوفر الوصول إلى خيارات التحجيم للمحور. |
| [getShapeType()](#getShapeType) |  |
| [getStyleItem()](#getStyleItem) |  |
| [getTickLabels()](#getTickLabels) | يوفر الوصول إلى خصائص تسميات علامات المحور. |
| [getTickMarkSpacing()](#getTickMarkSpacing) | يحصل على الفاصل الزمني الذي تُرسم عنده العلامات. |
| [getTitle()](#getTitle) | يوفر الوصول إلى خصائص عنوان المحور. |
| [getTitleDeleted()](#getTitleDeleted) |  |
| [getTitlePosition()](#getTitlePosition) |  |
| [getType()](#getType) | يعيد نوع المحور. |
| [hasMajorGridlines()](#hasMajorGridlines) | يحصل على علم يشير إلى ما إذا كان للمحور خطوط شبكة رئيسية. |
| [hasMajorGridlines(boolean value)](#hasMajorGridlines-boolean) | يضبط علمًا يشير إلى ما إذا كان للمحور خطوط شبكة رئيسية. |
| [hasMinorGridlines()](#hasMinorGridlines) | يحصل على علم يشير إلى ما إذا كان للمحور خطوط شبكة فرعية. |
| [hasMinorGridlines(boolean value)](#hasMinorGridlines-boolean) | يضبط علمًا يشير إلى ما إذا كان للمحور خطوط شبكة فرعية. |
| [isFillSupported()](#isFillSupported) |  |
| [isFormatDefined()](#isFormatDefined) |  |
| [isInherited()](#isInherited) |  |
| [isVisible()](#isVisible) |  |
| [materializeSpPr()](#materializeSpPr) |  |
| [setAxisBetweenCategories(boolean value)](#setAxisBetweenCategories-boolean) | يضبط علمًا يشير إلى ما إذا كان محور القيم يعبر محور الفئة بين الفئات. |
| [setBaseTimeUnit(int value)](#setBaseTimeUnit-int) | يضبط أصغر وحدة زمنية يتم تمثيلها على محور الفئة الزمنية. |
| [setCategoryType(int value)](#setCategoryType-int) | يضبط نوع محور الفئة. |
| [setCrosses(int value)](#setCrosses-int) | يحدد كيفية عبور هذا المحور للمحور المتعامد. |
| [setCrossesAt(double value)](#setCrossesAt-double) | يحدد أين على المحور المتعامد يعبر المحور. |
| [setHidden(boolean value)](#setHidden-boolean) | يضبط علمًا يشير إلى ما إذا كان هذا المحور مخفيًا أم لا. |
| [setMajorTickMark(int value)](#setMajorTickMark-int) | يضبط علامات التحديد الرئيسية. |
| [setMajorUnit(double value)](#setMajorUnit-double) | يضبط المسافة بين علامات التحديد الرئيسية. |
| [setMajorUnitIsAuto(boolean value)](#setMajorUnitIsAuto-boolean) | يضبط علامة تشير إلى ما إذا كان يجب استخدام المسافة الافتراضية بين علامات التحديد الرئيسية. |
| [setMajorUnitScale(int value)](#setMajorUnitScale-int) | يضبط قيمة المقياس لعلامات التحديد الرئيسية على محور الفئة الزمنية. |
| [setMinorTickMark(int value)](#setMinorTickMark-int) | يضبط علامات التحديد الثانوية للمحور. |
| [setMinorUnit(double value)](#setMinorUnit-double) | يضبط المسافة بين علامات التحديد الثانوية. |
| [setMinorUnitIsAuto(boolean value)](#setMinorUnitIsAuto-boolean) | يضبط علامة تشير إلى ما إذا كان يجب استخدام المسافة الافتراضية بين علامات التحديد الثانوية. |
| [setMinorUnitScale(int value)](#setMinorUnitScale-int) | يضبط قيمة المقياس لعلامات التحديد الثانوية على محور الفئة الزمنية. |
| [setReverseOrder(boolean value)](#setReverseOrder-boolean) | يضبط علامة تشير إلى ما إذا كان يجب عرض قيم المحور بترتيب عكسي، أي. |
| [setShapeType(int value)](#setShapeType-int) |  |
| [setTickMarkSpacing(int value)](#setTickMarkSpacing-int) | يضبط الفاصل الزمني الذي تُرسم عنده علامات التحديد. |
| [setTitleDeleted(boolean value)](#setTitleDeleted-boolean) |  |
### getAxisBetweenCategories() {#getAxisBetweenCategories}
```
public boolean getAxisBetweenCategories()
```


يحصل على علم يشير إلى ما إذا كان محور القيمة يعبر محور الفئة بين الفئات.

 **Remarks:** 

الخاصية لها تأثير فقط على محاور القيم. لا يتم دعمها في المخططات الجديدة لـ MS Office 2016.

 **Examples:** 

يظهر كيفية جعل محور الرسم يتقاطع عند موقع مخصص.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // For column charts, the Y-axis crosses at zero by default,
 // which means that columns for all values below zero point down to represent negative values.
 // We can set a different value for the Y-axis crossing. In this case, we will set it to 3.
 ChartAxis axis = chart.getAxisX();
 axis.setCrosses(AxisCrosses.CUSTOM);
 axis.setCrossesAt(3.0);
 axis.setAxisBetweenCategories(true);

 doc.save(getArtifactsDir() + "Charts.AxisCross.docx");
 
```

**Returns:**
boolean - علامة تشير إلى ما إذا كان محور القيمة يتقاطع مع محور الفئة بين الفئات.
### getBaseTimeUnit() {#getBaseTimeUnit}
```
public int getBaseTimeUnit()
```


يحصل على أصغر وحدة زمنية ممثلة على محور الفئة الزمنية.

 **Remarks:** 

الخاصية لها تأثير فقط على محاور الفئة الزمنية.

 **Examples:** 

يظهر كيفية إدراج مخطط بقيم التاريخ/الوقت.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 Date datetimeMin = DocumentHelper.createDate(2017, 11, 5);
 xAxis.getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(2017, 12, 3);
 xAxis.getScaling().setMaximum(new AxisBound(datetimeMax));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Returns:**
int - أصغر وحدة زمنية يتم تمثيلها على محور الفئة الزمنية. القيمة المرجعة هي واحدة من ثوابت [AxisTimeUnit](../../com.aspose.words/axistimeunit/).
### getCategoryType() {#getCategoryType}
```
public int getCategoryType()
```


يحصل على نوع محور الفئة.

 **Remarks:** 

فقط فئات النص ( [AxisCategoryType.CATEGORY](../../com.aspose.words/axiscategorytype/\#CATEGORY)) مسموح بها في المخططات الجديدة لـ MS Office 2016.

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
int - نوع محور الفئة. القيمة المرجعة هي واحدة من ثوابت [AxisCategoryType](../../com.aspose.words/axiscategorytype/).
### getCrosses() {#getCrosses}
```
public int getCrosses()
```


يحدد كيفية عبور هذا المحور للمحور المتعامد.

 **Remarks:** 

القيمة الافتراضية هي [AxisCrosses.AUTOMATIC](../../com.aspose.words/axiscrosses/\#AUTOMATIC).

الخاصية غير مدعومة في المخططات الجديدة لـ MS Office 2016.

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
int - القيمة الصحيحة المقابلة. القيمة المرجعة هي واحدة من ثوابت [AxisCrosses](../../com.aspose.words/axiscrosses/).
### getCrossesAt() {#getCrossesAt}
```
public double getCrossesAt()
```


يحدد أين على المحور المتعامد يعبر المحور.

 **Remarks:** 

الخاصية لها تأثير فقط إذا تم تعيين [getCrosses()](../../com.aspose.words/chartaxis/\#getCrosses) / [setCrosses(int)](../../com.aspose.words/chartaxis/\#setCrosses-int) إلى [AxisCrosses.CUSTOM](../../com.aspose.words/axiscrosses/\#CUSTOM). لا يتم دعمها في المخططات الجديدة لـ MS Office 2016.

الوحدات تُحدد وفقًا لنوع المحور. عندما يكون المحور محور قيمة، تكون قيمة الخاصية عددًا عشريًا على محور القيمة. عندما يكون المحور محور فئة زمنية، تُعرّف القيمة كعدد صحيح من الأيام بالنسبة إلى التاريخ الأساسي (30/12/1899). بالنسبة لمحور فئة نصية، تكون القيمة رقم فئة صحيح، يبدأ بـ 1 كالفئة الأولى.

 **Examples:** 

يظهر كيفية جعل محور الرسم يتقاطع عند موقع مخصص.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // For column charts, the Y-axis crosses at zero by default,
 // which means that columns for all values below zero point down to represent negative values.
 // We can set a different value for the Y-axis crossing. In this case, we will set it to 3.
 ChartAxis axis = chart.getAxisX();
 axis.setCrosses(AxisCrosses.CUSTOM);
 axis.setCrossesAt(3.0);
 axis.setAxisBetweenCategories(true);

 doc.save(getArtifactsDir() + "Charts.AxisCross.docx");
 
```

**Returns:**
double - القيمة المقابلة للـ double.
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
### getDisplayUnit() {#getDisplayUnit}
```
public AxisDisplayUnit getDisplayUnit()
```


يحدد قيمة التحجيم لوحدات العرض لمحور القيم.

 **Remarks:** 

الخاصية لها تأثير فقط على محاور القيم.

 **Examples:** 

يظهر كيفية تعديل علامات الفواصل والقيم المعروضة لمحور المخطط.

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
[AxisDisplayUnit](../../com.aspose.words/axisdisplayunit/) - The corresponding [AxisDisplayUnit](../../com.aspose.words/axisdisplayunit/) value.
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


يرجع المستند الذي يحتوي على المخطط الأصلي.

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
[DocumentBase](../../com.aspose.words/documentbase/) - The document containing the parent chart.
### getFormat() {#getFormat}
```
public ChartFormat getFormat()
```


يوفر الوصول إلى تنسيق الخط للمحور وتعبئة تسميات العلامات.

 **Remarks:** 

يمكن تغيير تعبئة علامات التحديد في المخطط فقط للمخططات السابقة لـ Word 2016. مخططات Word 2016 لا تدعم ذلك.

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
[ChartFormat](../../com.aspose.words/chartformat/) - The corresponding [ChartFormat](../../com.aspose.words/chartformat/) value.
### getHidden() {#getHidden}
```
public boolean getHidden()
```


يحصل على علم يشير إلى ما إذا كان هذا المحور مخفيًا أم لا.

 **Remarks:** 

القيمة الافتراضية هي false .

 **Examples:** 

يظهر كيفية إخفاء محاور المخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with categories for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("AW Series 1",
         new String[]{"Item 1", "Item 2", "Item 3", "Item 4", "Item 5"},
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2});

 // Hide the chart axes to simplify the appearance of the chart.
 chart.getAxisX().setHidden(true);
 chart.getAxisY().setHidden(true);

 doc.save(getArtifactsDir() + "Charts.HideChartAxis.docx");
 
```

**Returns:**
boolean - علامة تشير إلى ما إذا كان هذا المحور مخفيًا أم لا.
### getMajorTickMark() {#getMajorTickMark}
```
public int getMajorTickMark()
```


يحصل على العلامات الرئيسية.

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
int - العلامات الرئيسية للمحاور. القيمة المرجعة هي واحدة من ثوابت [AxisTickMark](../../com.aspose.words/axistickmark/).
### getMajorUnit() {#getMajorUnit}
```
public double getMajorUnit()
```


يحصل على المسافة بين العلامات الرئيسية.

 **Remarks:** 

النطاق الصالح للقيمة هو أكبر من الصفر. الخاصية لها تأثير على محاور الفئة الزمنية والمحاور القيمية.

تعيين هذه الخاصية يضبط الخاصية [getMajorUnitIsAuto()](../../com.aspose.words/chartaxis/\#getMajorUnitIsAuto) / [setMajorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis/\#setMajorUnitIsAuto-boolean) إلى false .

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
double - المسافة بين العلامات الرئيسية.
### getMajorUnitIsAuto() {#getMajorUnitIsAuto}
```
public boolean getMajorUnitIsAuto()
```


يحصل على علم يشير إلى ما إذا كان يجب استخدام المسافة الافتراضية بين العلامات الرئيسية.

 **Remarks:** 

الخاصية لها تأثير على محاور الفئة الزمنية والمحاور القيمية.

 **Examples:** 

يظهر كيفية تعديل علامات الفواصل والقيم المعروضة لمحور المخطط.

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
boolean - علم يشير إلى ما إذا كان يجب استخدام المسافة الافتراضية بين العلامات الرئيسية.
### getMajorUnitScale() {#getMajorUnitScale}
```
public int getMajorUnitScale()
```


يحصل على قيمة المقياس للعلامات الرئيسية على محور الفئة الزمنية.

 **Remarks:** 

الخاصية لها تأثير فقط على محاور الفئة الزمنية.

 **Examples:** 

يظهر كيفية تعديل علامات الفواصل والقيم المعروضة لمحور المخطط.

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
int - قيمة المقياس للعلامات الرئيسية على محور الفئة الزمنية. القيمة المرجعة هي واحدة من ثوابت [AxisTimeUnit](../../com.aspose.words/axistimeunit/).
### getMinorTickMark() {#getMinorTickMark}
```
public int getMinorTickMark()
```


يحصل على العلامات الفرعية للمحور.

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
int - العلامات الثانوية للمحور. القيمة المرجعة هي واحدة من ثوابت [AxisTickMark](../../com.aspose.words/axistickmark/).
### getMinorUnit() {#getMinorUnit}
```
public double getMinorUnit()
```


يحصل على المسافة بين العلامات الفرعية.

 **Remarks:** 

النطاق الصالح للقيمة هو أكبر من الصفر. الخاصية لها تأثير على محاور الفئة الزمنية والمحاور القيمية.

تعيين هذه الخاصية يضبط الخاصية [getMinorUnitIsAuto()](../../com.aspose.words/chartaxis/\#getMinorUnitIsAuto) / [setMinorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis/\#setMinorUnitIsAuto-boolean) إلى false .

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
double - المسافة بين العلامات الثانوية.
### getMinorUnitIsAuto() {#getMinorUnitIsAuto}
```
public boolean getMinorUnitIsAuto()
```


يحصل على علم يشير إلى ما إذا كان يجب استخدام المسافة الافتراضية بين العلامات الفرعية.

 **Remarks:** 

الخاصية لها تأثير على محاور الفئة الزمنية والمحاور القيمية.

 **Examples:** 

يظهر كيفية تعديل علامات الفواصل والقيم المعروضة لمحور المخطط.

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
boolean - علم يشير إلى ما إذا كان يجب استخدام المسافة الافتراضية بين العلامات الثانوية.
### getMinorUnitScale() {#getMinorUnitScale}
```
public int getMinorUnitScale()
```


يحصل على قيمة المقياس للعلامات الفرعية على محور الفئة الزمنية.

 **Remarks:** 

الخاصية لها تأثير فقط على محاور الفئة الزمنية.

 **Examples:** 

يظهر كيفية تعديل علامات الفواصل والقيم المعروضة لمحور المخطط.

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
int - قيمة المقياس للعلامات الثانوية على محور الفئة الزمنية. القيمة المرجعة هي واحدة من ثوابت [AxisTimeUnit](../../com.aspose.words/axistimeunit/).
### getNumberFormat() {#getNumberFormat}
```
public ChartNumberFormat getNumberFormat()
```


يعيد كائن [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) الذي يتيح تعريف تنسيقات الأرقام للمحور.

 **Examples:** 

يوضح كيفية تعيين التنسيق لقيم المخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series to the chart with categories for the X-axis,
 // and large respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{1900000.0, 850000.0, 2100000.0, 600000.0, 1500000.0});

 // Set the number format of the Y-axis tick labels to not group digits with commas.
 chart.getAxisY().getNumberFormat().setFormatCode("#,##0");

 // This flag can override the above value and draw the number format from the source cell.
 Assert.assertFalse(chart.getAxisY().getNumberFormat().isLinkedToSource());

 doc.save(getArtifactsDir() + "Charts.SetNumberFormatToChartAxis.docx");
 
```

**Returns:**
[ChartNumberFormat](../../com.aspose.words/chartnumberformat/) - A [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) object that allows defining number formats for the axis.
### getRelativeFontSize(int chartFontSize) {#getRelativeFontSize-int}
```
public int getRelativeFontSize(int chartFontSize)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartFontSize | int |  |

**Returns:**
int
### getReverseOrder() {#getReverseOrder}
```
public boolean getReverseOrder()
```


يحصل على علم يشير إلى ما إذا كان يجب عرض قيم المحور بترتيب عكسي، أي من الحد الأقصى إلى الحد الأدنى.

 **Remarks:** 

الخاصية غير مدعومة في المخططات الجديدة لـ MS Office 2016. القيمة الافتراضية هي false .

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
boolean - علم يشير إلى ما إذا كان يجب عرض قيم المحور بترتيب عكسي، أي.
### getScaling() {#getScaling}
```
public AxisScaling getScaling()
```


يوفر الوصول إلى خيارات التحجيم للمحور.

 **Examples:** 

يظهر كيفية إدراج مخطط بقيم التاريخ/الوقت.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 Date datetimeMin = DocumentHelper.createDate(2017, 11, 5);
 xAxis.getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(2017, 12, 3);
 xAxis.getScaling().setMaximum(new AxisBound(datetimeMax));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Returns:**
[AxisScaling](../../com.aspose.words/axisscaling/) - The corresponding [AxisScaling](../../com.aspose.words/axisscaling/) value.
### getShapeType() {#getShapeType}
```
public int getShapeType()
```




**Returns:**
int
### getStyleItem() {#getStyleItem}
```
public int getStyleItem()
```




**Returns:**
int
### getTickLabels() {#getTickLabels}
```
public AxisTickLabels getTickLabels()
```


يوفر الوصول إلى خصائص تسميات علامات المحور.

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
[AxisTickLabels](../../com.aspose.words/axisticklabels/) - The corresponding [AxisTickLabels](../../com.aspose.words/axisticklabels/) value.
### getTickMarkSpacing() {#getTickMarkSpacing}
```
public int getTickMarkSpacing()
```


يحصل على الفاصل الزمني الذي تُرسم عنده العلامات.

 **Remarks:** 

الخاصية لها تأثير على محاور الفئات النصية والسلاسل. لا يتم دعمها في المخططات الجديدة لـ MS Office 2016.

النطاق الصالح للقيمة هو أكبر من أو يساوي 1.

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
int - الفاصل الزمني الذي تُرسم عنده العلامات.
### getTitle() {#getTitle}
```
public ChartAxisTitle getTitle()
```


يوفر الوصول إلى خصائص عنوان المحور.

 **Examples:** 

يوضح كيفية تعيين عنوان محور المخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 seriesColl.add("AW Series 1", new String[] { "AW Category 1", "AW Category 2" }, new double[] { 1.0, 2.0 });

 // Set axis title.
 ChartAxisTitle chartAxisXTitle = chart.getAxisX().getTitle();
 chartAxisXTitle.setText("Categories");
 chartAxisXTitle.setShow(true);
 ChartAxisTitle chartAxisYTitle = chart.getAxisY().getTitle();
 chartAxisYTitle.setText("Values");
 chartAxisYTitle.setShow(true);
 chartAxisYTitle.setOverlay(true);
 chartAxisYTitle.getFont().setSize(12.0);
 chartAxisYTitle.getFont().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.ChartAxisTitle.docx");
 
```

**Returns:**
[ChartAxisTitle](../../com.aspose.words/chartaxistitle/) - The corresponding [ChartAxisTitle](../../com.aspose.words/chartaxistitle/) value.
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
### getType() {#getType}
```
public int getType()
```


يعيد نوع المحور.

 **Examples:** 

يوضح كيفية إنشاء نوع مناسب من سلاسل المخطط لنوع الرسم البياني.

```

 public void chartSeriesCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // There are several ways of populating a chart's series collection.
     // Different series schemas are intended for different chart types.
     // 1 -  Column chart with columns grouped and banded along the X-axis by category:
     Chart chart = appendChart(builder, ChartType.COLUMN, 500.0, 300.0);

     String[] categories = {"Category 1", "Category 2", "Category 3"};

     // Insert two series of decimal values containing a value for each respective category.
     // This column chart will have three groups, each with two columns.
     chart.getSeries().add("Series 1", categories, new double[]{76.6, 82.1, 91.6});
     chart.getSeries().add("Series 2", categories, new double[]{64.2, 79.5, 94.0});

     // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 2 -  Area chart with dates distributed along the X-axis:
     chart = appendChart(builder, ChartType.AREA, 500.0, 300.0);

     Date[] dates = {DocumentHelper.createDate(2014, 3, 31),
             DocumentHelper.createDate(2017, 1, 23),
             DocumentHelper.createDate(2017, 6, 18),
             DocumentHelper.createDate(2019, 11, 22),
             DocumentHelper.createDate(2020, 9, 7)
     };

     // Insert a series with a decimal value for each respective date.
     // The dates will be distributed along a linear X-axis,
     // and the values added to this series will create data points.
     chart.getSeries().add("Series 1", dates, new double[]{15.8, 21.5, 22.9, 28.7, 33.1});

     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 3 -  2D scatter plot:
     chart = appendChart(builder, ChartType.SCATTER, 500.0, 300.0);

     // Each series will need two decimal arrays of equal length.
     // The first array contains X-values, and the second contains corresponding Y-values
     // of data points on the chart's graph.
     chart.getSeries().add("Series 1",
             new double[]{3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6},
             new double[]{3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9});
     chart.getSeries().add("Series 2",
             new double[]{2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3},
             new double[]{7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6});

     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 4 -  Bubble chart:
     chart = appendChart(builder, ChartType.BUBBLE, 500.0, 300.0);

     // Each series will need three decimal arrays of equal length.
     // The first array contains X-values, the second contains corresponding Y-values,
     // and the third contains diameters for each of the graph's data points.
     chart.getSeries().add("Series 1",
             new double[]{1.1, 5.0, 9.8},
             new double[]{1.2, 4.9, 9.9},
             new double[]{2.0, 4.0, 8.0});

     doc.save(getArtifactsDir() + "Charts.ChartSeriesCollection.docx");
 }

 /// 
 /// Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data.
 /// 
 private static Chart appendChart(DocumentBuilder builder, int chartType, double width, double height) throws Exception {
     Shape chartShape = builder.insertChart(chartType, width, height);
     Chart chart = chartShape.getChart();
     chart.getSeries().clear();
     return chart;
 }
 
```

**Returns:**
int - نوع المحور. القيمة المرجعة هي واحدة من ثوابت [ChartAxisType](../../com.aspose.words/chartaxistype/).
### hasMajorGridlines() {#hasMajorGridlines}
```
public boolean hasMajorGridlines()
```


يحصل على علم يشير إلى ما إذا كان للمحور خطوط شبكة رئيسية.

 **Examples:** 

يظهر كيفية إدراج مخطط بقيم التاريخ/الوقت.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 Date datetimeMin = DocumentHelper.createDate(2017, 11, 5);
 xAxis.getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(2017, 12, 3);
 xAxis.getScaling().setMaximum(new AxisBound(datetimeMax));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Returns:**
boolean - علم يشير إلى ما إذا كان للمحور خطوط شبكة رئيسية.
### hasMajorGridlines(boolean value) {#hasMajorGridlines-boolean}
```
public void hasMajorGridlines(boolean value)
```


يضبط علمًا يشير إلى ما إذا كان للمحور خطوط شبكة رئيسية.

 **Examples:** 

يظهر كيفية إدراج مخطط بقيم التاريخ/الوقت.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 Date datetimeMin = DocumentHelper.createDate(2017, 11, 5);
 xAxis.getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(2017, 12, 3);
 xAxis.getScaling().setMaximum(new AxisBound(datetimeMax));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علم يشير إلى ما إذا كان للمحور خطوط شبكة رئيسية. |

### hasMinorGridlines() {#hasMinorGridlines}
```
public boolean hasMinorGridlines()
```


يحصل على علم يشير إلى ما إذا كان للمحور خطوط شبكة فرعية.

 **Examples:** 

يظهر كيفية إدراج مخطط بقيم التاريخ/الوقت.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 Date datetimeMin = DocumentHelper.createDate(2017, 11, 5);
 xAxis.getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(2017, 12, 3);
 xAxis.getScaling().setMaximum(new AxisBound(datetimeMax));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Returns:**
boolean - علم يشير إلى ما إذا كان للمحور خطوط شبكة ثانوية.
### hasMinorGridlines(boolean value) {#hasMinorGridlines-boolean}
```
public void hasMinorGridlines(boolean value)
```


يضبط علمًا يشير إلى ما إذا كان للمحور خطوط شبكة فرعية.

 **Examples:** 

يظهر كيفية إدراج مخطط بقيم التاريخ/الوقت.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 Date datetimeMin = DocumentHelper.createDate(2017, 11, 5);
 xAxis.getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(2017, 12, 3);
 xAxis.getScaling().setMaximum(new AxisBound(datetimeMax));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علم يشير إلى ما إذا كان للمحور خطوط شبكة ثانوية. |

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
### isVisible() {#isVisible}
```
public boolean isVisible()
```




**Returns:**
boolean
### materializeSpPr() {#materializeSpPr}
```
public void materializeSpPr()
```




### setAxisBetweenCategories(boolean value) {#setAxisBetweenCategories-boolean}
```
public void setAxisBetweenCategories(boolean value)
```


يضبط علمًا يشير إلى ما إذا كان محور القيم يعبر محور الفئة بين الفئات.

 **Remarks:** 

الخاصية لها تأثير فقط على محاور القيم. لا يتم دعمها في المخططات الجديدة لـ MS Office 2016.

 **Examples:** 

يظهر كيفية جعل محور الرسم يتقاطع عند موقع مخصص.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // For column charts, the Y-axis crosses at zero by default,
 // which means that columns for all values below zero point down to represent negative values.
 // We can set a different value for the Y-axis crossing. In this case, we will set it to 3.
 ChartAxis axis = chart.getAxisX();
 axis.setCrosses(AxisCrosses.CUSTOM);
 axis.setCrossesAt(3.0);
 axis.setAxisBetweenCategories(true);

 doc.save(getArtifactsDir() + "Charts.AxisCross.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علم يشير إلى ما إذا كان محور القيم يعبر محور الفئة بين الفئات. |

### setBaseTimeUnit(int value) {#setBaseTimeUnit-int}
```
public void setBaseTimeUnit(int value)
```


يضبط أصغر وحدة زمنية يتم تمثيلها على محور الفئة الزمنية.

 **Remarks:** 

الخاصية لها تأثير فقط على محاور الفئة الزمنية.

 **Examples:** 

يظهر كيفية إدراج مخطط بقيم التاريخ/الوقت.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 Date datetimeMin = DocumentHelper.createDate(2017, 11, 5);
 xAxis.getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(2017, 12, 3);
 xAxis.getScaling().setMaximum(new AxisBound(datetimeMax));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | أصغر وحدة زمنية ممثلة على محور الفئة الزمنية. يجب أن تكون القيمة واحدة من ثوابت [AxisTimeUnit](../../com.aspose.words/axistimeunit/). |

### setCategoryType(int value) {#setCategoryType-int}
```
public void setCategoryType(int value)
```


يضبط نوع محور الفئة.

 **Remarks:** 

فقط فئات النص ( [AxisCategoryType.CATEGORY](../../com.aspose.words/axiscategorytype/\#CATEGORY)) مسموح بها في المخططات الجديدة لـ MS Office 2016.

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | نوع محور الفئة. يجب أن تكون القيمة واحدة من ثوابت [AxisCategoryType](../../com.aspose.words/axiscategorytype/). |

### setCrosses(int value) {#setCrosses-int}
```
public void setCrosses(int value)
```


يحدد كيفية عبور هذا المحور للمحور المتعامد.

 **Remarks:** 

القيمة الافتراضية هي [AxisCrosses.AUTOMATIC](../../com.aspose.words/axiscrosses/\#AUTOMATIC).

الخاصية غير مدعومة في المخططات الجديدة لـ MS Office 2016.

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة الصحيحة int المقابلة. يجب أن تكون القيمة واحدة من ثوابت [AxisCrosses](../../com.aspose.words/axiscrosses/). |

### setCrossesAt(double value) {#setCrossesAt-double}
```
public void setCrossesAt(double value)
```


يحدد أين على المحور المتعامد يعبر المحور.

 **Remarks:** 

الخاصية لها تأثير فقط إذا تم تعيين [getCrosses()](../../com.aspose.words/chartaxis/\#getCrosses) / [setCrosses(int)](../../com.aspose.words/chartaxis/\#setCrosses-int) إلى [AxisCrosses.CUSTOM](../../com.aspose.words/axiscrosses/\#CUSTOM). لا يتم دعمها في المخططات الجديدة لـ MS Office 2016.

الوحدات تُحدد وفقًا لنوع المحور. عندما يكون المحور محور قيمة، تكون قيمة الخاصية عددًا عشريًا على محور القيمة. عندما يكون المحور محور فئة زمنية، تُعرّف القيمة كعدد صحيح من الأيام بالنسبة إلى التاريخ الأساسي (30/12/1899). بالنسبة لمحور فئة نصية، تكون القيمة رقم فئة صحيح، يبدأ بـ 1 كالفئة الأولى.

 **Examples:** 

يظهر كيفية جعل محور الرسم يتقاطع عند موقع مخصص.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // For column charts, the Y-axis crosses at zero by default,
 // which means that columns for all values below zero point down to represent negative values.
 // We can set a different value for the Y-axis crossing. In this case, we will set it to 3.
 ChartAxis axis = chart.getAxisX();
 axis.setCrosses(AxisCrosses.CUSTOM);
 axis.setCrossesAt(3.0);
 axis.setAxisBetweenCategories(true);

 doc.save(getArtifactsDir() + "Charts.AxisCross.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة العشرية المقابلة. |

### setHidden(boolean value) {#setHidden-boolean}
```
public void setHidden(boolean value)
```


يضبط علمًا يشير إلى ما إذا كان هذا المحور مخفيًا أم لا.

 **Remarks:** 

القيمة الافتراضية هي false .

 **Examples:** 

يظهر كيفية إخفاء محاور المخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with categories for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("AW Series 1",
         new String[]{"Item 1", "Item 2", "Item 3", "Item 4", "Item 5"},
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2});

 // Hide the chart axes to simplify the appearance of the chart.
 chart.getAxisX().setHidden(true);
 chart.getAxisY().setHidden(true);

 doc.save(getArtifactsDir() + "Charts.HideChartAxis.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علامة تشير إلى ما إذا كان هذا المحور مخفيًا أم لا. |

### setMajorTickMark(int value) {#setMajorTickMark-int}
```
public void setMajorTickMark(int value)
```


يضبط علامات التحديد الرئيسية.

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | علامات الفواصل الرئيسية. يجب أن تكون القيمة واحدة من ثوابت [AxisTickMark](../../com.aspose.words/axistickmark/). |

### setMajorUnit(double value) {#setMajorUnit-double}
```
public void setMajorUnit(double value)
```


يضبط المسافة بين علامات التحديد الرئيسية.

 **Remarks:** 

النطاق الصالح للقيمة هو أكبر من الصفر. الخاصية لها تأثير على محاور الفئة الزمنية والمحاور القيمية.

تعيين هذه الخاصية يضبط الخاصية [getMajorUnitIsAuto()](../../com.aspose.words/chartaxis/\#getMajorUnitIsAuto) / [setMajorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis/\#setMajorUnitIsAuto-boolean) إلى false .

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | المسافة بين علامات الفواصل الرئيسية. |

### setMajorUnitIsAuto(boolean value) {#setMajorUnitIsAuto-boolean}
```
public void setMajorUnitIsAuto(boolean value)
```


يضبط علامة تشير إلى ما إذا كان يجب استخدام المسافة الافتراضية بين علامات التحديد الرئيسية.

 **Remarks:** 

الخاصية لها تأثير على محاور الفئة الزمنية والمحاور القيمية.

 **Examples:** 

يظهر كيفية تعديل علامات الفواصل والقيم المعروضة لمحور المخطط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علامة تشير إلى ما إذا كان يجب استخدام المسافة الافتراضية بين علامات الفواصل الرئيسية. |

### setMajorUnitScale(int value) {#setMajorUnitScale-int}
```
public void setMajorUnitScale(int value)
```


يضبط قيمة المقياس لعلامات التحديد الرئيسية على محور الفئة الزمنية.

 **Remarks:** 

الخاصية لها تأثير فقط على محاور الفئة الزمنية.

 **Examples:** 

يظهر كيفية تعديل علامات الفواصل والقيم المعروضة لمحور المخطط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | قيمة المقياس لعلامات الفواصل الرئيسية على محور الفئة الزمنية. يجب أن تكون القيمة واحدة من ثوابت [AxisTimeUnit](../../com.aspose.words/axistimeunit/). |

### setMinorTickMark(int value) {#setMinorTickMark-int}
```
public void setMinorTickMark(int value)
```


يضبط علامات التحديد الثانوية للمحور.

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | علامات الفواصل الفرعية للمحور. يجب أن تكون القيمة واحدة من ثوابت [AxisTickMark](../../com.aspose.words/axistickmark/). |

### setMinorUnit(double value) {#setMinorUnit-double}
```
public void setMinorUnit(double value)
```


يضبط المسافة بين علامات التحديد الثانوية.

 **Remarks:** 

النطاق الصالح للقيمة هو أكبر من الصفر. الخاصية لها تأثير على محاور الفئة الزمنية والمحاور القيمية.

تعيين هذه الخاصية يضبط الخاصية [getMinorUnitIsAuto()](../../com.aspose.words/chartaxis/\#getMinorUnitIsAuto) / [setMinorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis/\#setMinorUnitIsAuto-boolean) إلى false .

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | المسافة بين علامات الفواصل الفرعية. |

### setMinorUnitIsAuto(boolean value) {#setMinorUnitIsAuto-boolean}
```
public void setMinorUnitIsAuto(boolean value)
```


يضبط علامة تشير إلى ما إذا كان يجب استخدام المسافة الافتراضية بين علامات التحديد الثانوية.

 **Remarks:** 

الخاصية لها تأثير على محاور الفئة الزمنية والمحاور القيمية.

 **Examples:** 

يظهر كيفية تعديل علامات الفواصل والقيم المعروضة لمحور المخطط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علامة تشير إلى ما إذا كان يجب استخدام المسافة الافتراضية بين علامات الفواصل الفرعية. |

### setMinorUnitScale(int value) {#setMinorUnitScale-int}
```
public void setMinorUnitScale(int value)
```


يضبط قيمة المقياس لعلامات التحديد الثانوية على محور الفئة الزمنية.

 **Remarks:** 

الخاصية لها تأثير فقط على محاور الفئة الزمنية.

 **Examples:** 

يظهر كيفية تعديل علامات الفواصل والقيم المعروضة لمحور المخطط.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | قيمة المقياس لعلامات الفواصل الفرعية على محور الفئة الزمنية. يجب أن تكون القيمة واحدة من ثوابت [AxisTimeUnit](../../com.aspose.words/axistimeunit/). |

### setReverseOrder(boolean value) {#setReverseOrder-boolean}
```
public void setReverseOrder(boolean value)
```


يضبط علامة تشير إلى ما إذا كان يجب عرض قيم المحور بترتيب عكسي، أي من الحد الأقصى إلى الحد الأدنى.

 **Remarks:** 

الخاصية غير مدعومة في المخططات الجديدة لـ MS Office 2016. القيمة الافتراضية هي false .

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علامة تشير إلى ما إذا كان يجب عرض قيم المحور بترتيب عكسي، أي. |

### setShapeType(int value) {#setShapeType-int}
```
public void setShapeType(int value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int |  |

### setTickMarkSpacing(int value) {#setTickMarkSpacing-int}
```
public void setTickMarkSpacing(int value)
```


يضبط الفاصل الزمني الذي تُرسم عنده علامات التحديد.

 **Remarks:** 

الخاصية لها تأثير على محاور الفئات النصية والسلاسل. لا يتم دعمها في المخططات الجديدة لـ MS Office 2016.

النطاق الصالح للقيمة هو أكبر من أو يساوي 1.

 **Examples:** 

يظهر كيفية إدراج مخطط وتعديل مظهر محاوره.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | الفاصل الزمني الذي تُرسم عنده علامات الفواصل. |

### setTitleDeleted(boolean value) {#setTitleDeleted-boolean}
```
public void setTitleDeleted(boolean value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean |  |

