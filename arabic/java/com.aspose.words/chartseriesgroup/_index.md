---
title: "ChartSeriesGroup"
linktitle: "ChartSeriesGroup"
second_title: "Aspose.Words لـ Java"
description: "يمثل خصائص مجموعة سلاسل المخطط التي هي خصائص سلاسل المخطط من نفس النوع المرتبطة بنفس المحاور في Java."
type: docs
weight: 87
url: /ar/java/com.aspose.words/chartseriesgroup/
---

**Inheritance:**
java.lang.Object
```
public class ChartSeriesGroup
```

يمثل خصائص مجموعة سلاسل المخطط، أي خصائص سلاسل المخطط من نفس النوع المرتبطة بنفس المحاور.

 **Remarks:** 

تحتوي المخططات المركبة على مجموعات متعددة من سلاسل المخطط، مع مجموعة منفصلة لكل نوع سلسلة.

كما يمكنك إنشاء مجموعة سلاسل مخطط لتعيين محاور ثانوية لسلسلة أو أكثر من سلاسل المخطط.

للتعرف على المزيد، زر مقالة توثيق [ Working with Charts ][Working with Charts].

 **Examples:** 

يوضح كيفية العمل مع المحور الثانوي للمخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getAxisGroup()](#getAxisGroup) | يحصل على مجموعة المحاور التي تنتمي إليها مجموعة السلاسل هذه. |
| [getAxisX()](#getAxisX) | يوفر الوصول إلى خصائص المحور X لمجموعة السلاسل هذه. |
| [getAxisY()](#getAxisY) | يوفر الوصول إلى خصائص المحور Y لمجموعة السلاسل هذه. |
| [getBubbleScale()](#getBubbleScale) | يحصل على حجم الفقاعات كنسبة مئوية من حجمها الافتراضي. |
| [getDoughnutHoleSize()](#getDoughnutHoleSize) | يحصل على حجم الفتحة في مخطط الدونات الأب كنسبة مئوية. |
| [getFirstSliceAngle()](#getFirstSliceAngle) | يحصل على الزاوية، بالدرجات، للقطعة الأولى في مخطط الفطيرة الأب. |
| [getGapWidth()](#getGapWidth) | يحصل على نسبة عرض الفجوة بين عناصر المخطط. |
| [getOverlap()](#getOverlap) | يحصل على النسبة المئوية لمدى تداخل أشرطة أو أعمدة السلسلة. |
| [getSecondSectionSize()](#getSecondSectionSize) | يحصل على حجم القسم الثانوي لمخطط الفطيرة كنسبة مئوية. |
| [getSeries()](#getSeries) | يحصل على مجموعة من السلاسل التي تنتمي إلى مجموعة السلاسل هذه. |
| [getSeriesType()](#getSeriesType) | يحصل على نوع سلاسل المخطط المتضمنة في هذه المجموعة. |
| [setAxisGroup(int value)](#setAxisGroup-int) | يضبط مجموعة المحاور التي تنتمي إليها مجموعة السلاسل هذه. |
| [setBubbleScale(int value)](#setBubbleScale-int) | يضبط حجم الفقاعات كنسبة مئوية من حجمها الافتراضي. |
| [setDoughnutHoleSize(int value)](#setDoughnutHoleSize-int) | يضبط حجم الفتحة في مخطط الدونات الأب كنسبة مئوية. |
| [setFirstSliceAngle(int value)](#setFirstSliceAngle-int) | يضبط الزاوية، بالدرجات، للقطعة الأولى في مخطط الفطيرة الأب. |
| [setGapWidth(int value)](#setGapWidth-int) | يضبط نسبة عرض الفجوة بين عناصر المخطط. |
| [setOverlap(int value)](#setOverlap-int) | يضبط النسبة المئوية لمدى تداخل أشرطة أو أعمدة السلسلة. |
| [setSecondSectionSize(int value)](#setSecondSectionSize-int) | يضبط حجم القسم الثانوي لمخطط الفطيرة كنسبة مئوية. |
### getAxisGroup() {#getAxisGroup}
```
public int getAxisGroup()
```


يحصل على مجموعة المحاور التي تنتمي إليها مجموعة السلاسل هذه.

 **Examples:** 

يوضح كيفية العمل مع المحور الثانوي للمخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```

**Returns:**
int - مجموعة المحاور التي تنتمي إليها مجموعة السلاسل هذه. القيمة المرجعة هي واحدة من ثوابت [AxisGroup](../../com.aspose.words/axisgroup/) constants.
### getAxisX() {#getAxisX}
```
public ChartAxis getAxisX()
```


يوفر الوصول إلى خصائص المحور X لمجموعة السلاسل هذه.

 **Examples:** 

يوضح كيفية العمل مع المحور الثانوي للمخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```

**Returns:**
[ChartAxis](../../com.aspose.words/chartaxis/) - The corresponding [ChartAxis](../../com.aspose.words/chartaxis/) value.
### getAxisY() {#getAxisY}
```
public ChartAxis getAxisY()
```


يوفر الوصول إلى خصائص المحور Y لمجموعة السلاسل هذه.

 **Examples:** 

يوضح كيفية العمل مع المحور الثانوي للمخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```

**Returns:**
[ChartAxis](../../com.aspose.words/chartaxis/) - The corresponding [ChartAxis](../../com.aspose.words/chartaxis/) value.
### getBubbleScale() {#getBubbleScale}
```
public int getBubbleScale()
```


يحصل على حجم الفقاعات كنسبة مئوية من حجمها الافتراضي.

 **Remarks:** 

ينطبق فقط على مجموعات السلاسل من نوعي [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE) و [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D).

نطاق القيم المقبولة هو من 0 إلى 300 شاملًا. القيمة الافتراضية هي 100.

 **Examples:** 

عرض كيفية ضبط حجم الفقاعات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bubble 3D chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE_3_D, 450.0, 250.0);
 ChartSeriesGroup seriesGroup = shape.getChart().getSeriesGroups().get(0);

 // Set bubble scale to 200%.
 seriesGroup.setBubbleScale(200);

 doc.save(getArtifactsDir() + "Charts.BubbleScale.docx");
 
```

**Returns:**
int - حجم الفقاعات كنسبة مئوية من حجمها الافتراضي.
### getDoughnutHoleSize() {#getDoughnutHoleSize}
```
public int getDoughnutHoleSize()
```


يحصل على حجم الفتحة في مخطط الدونات الأب كنسبة مئوية.

 **Remarks:** 

ينطبق فقط على مجموعات السلاسل من نوع [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT).

نطاق القيم المقبولة هو من 0 إلى 90 شاملًا. القيمة الافتراضية هي 75.

 **Examples:** 

يعرض كيفية إنشاء وتنسيق مخطط الدونات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.DOUGHNUT, 400.0, 400.0);
 Chart chart = shape.getChart();
 // Delete the default generated series.
 chart.getSeries().clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 chart.getSeries().add("Series 1", categories, new double[] { 4.0, 2.0, 5.0 });

 // Format the Doughnut chart.
 ChartSeriesGroup seriesGroup = chart.getSeriesGroups().get(0);
 seriesGroup.setDoughnutHoleSize(10);
 seriesGroup.setFirstSliceAngle(270);

 doc.save(getArtifactsDir() + "Charts.DoughnutChart.docx");
 
```

**Returns:**
int - حجم الفتحة في مخطط الدونات الأصلي كنسبة مئوية.
### getFirstSliceAngle() {#getFirstSliceAngle}
```
public int getFirstSliceAngle()
```


يحصل على الزاوية، بالدرجات، للقطعة الأولى في مخطط الفطيرة الأب.

 **Remarks:** 

ينطبق على مجموعات السلاسل من الأنواع [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D) و[ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT) الأنواع.

النطاق المقبول للقيم هو من 0 إلى 360 شاملًا. القيمة الافتراضية هي 0.

 **Examples:** 

يعرض كيفية إنشاء وتنسيق مخطط الدونات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.DOUGHNUT, 400.0, 400.0);
 Chart chart = shape.getChart();
 // Delete the default generated series.
 chart.getSeries().clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 chart.getSeries().add("Series 1", categories, new double[] { 4.0, 2.0, 5.0 });

 // Format the Doughnut chart.
 ChartSeriesGroup seriesGroup = chart.getSeriesGroups().get(0);
 seriesGroup.setDoughnutHoleSize(10);
 seriesGroup.setFirstSliceAngle(270);

 doc.save(getArtifactsDir() + "Charts.DoughnutChart.docx");
 
```

**Returns:**
int - الزاوية، بالدرجات، للقطاع الأول في مخطط الفطيرة الأصلي.
### getGapWidth() {#getGapWidth}
```
public int getGapWidth()
```


يحصل على نسبة عرض الفجوة بين عناصر المخطط.

 **Remarks:** 

ينطبق فقط على مجموعات السلاسل من أنواع الشريط، العمود، فطيرة-على-شريط، فطيرة-على-فطيرة، المخطط التكراري، الصندوق والشارب، الشلال والقمع.

النطاق المقبول للقيم هو من 0 إلى 500 شاملًا. بالنسبة لمجموعات السلاسل القائمة على الشريط/العمود، تمثل الخاصية المسافة بين مجموعات الأشرطة كنسبة مئوية من عرضها. بالنسبة لمخططات فطيرة-على-فطيرة وبار-على-فطيرة، هذه هي المسافة بين الأقسام الأساسية والثانوية للمخطط.

 **Examples:** 

يوضح كيفية ضبط عرض الفجوة والتداخل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 450.0, 250.0);
 ChartSeriesGroup seriesGroup = shape.getChart().getSeriesGroups().get(0);

 // Set column gap width and overlap.
 seriesGroup.setGapWidth(450);
 seriesGroup.setOverlap(-75);

 doc.save(getArtifactsDir() + "Charts.ConfigureGapOverlap.docx");
 
```

**Returns:**
int - النسبة المئوية لعرض الفجوة بين عناصر المخطط.
### getOverlap() {#getOverlap}
```
public int getOverlap()
```


يحصل على النسبة المئوية لمدى تداخل أشرطة أو أعمدة السلسلة.

 **Remarks:** 

ينطبق على مجموعات السلاسل لجميع أنواع الشريط والعمود.

النطاق المقبول للقيم هو من -100 إلى 100 شاملًا. القيمة 0 تشير إلى عدم وجود مساحة بين الأشرطة/الأعمدة. إذا كانت القيمة -100، فإن المسافة بين الأشرطة/الأعمدة تساوي عرضها. القيمة 100 تعني أن الأشرطة/الأعمدة تتداخل تمامًا.

 **Examples:** 

يوضح كيفية ضبط عرض الفجوة والتداخل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 450.0, 250.0);
 ChartSeriesGroup seriesGroup = shape.getChart().getSeriesGroups().get(0);

 // Set column gap width and overlap.
 seriesGroup.setGapWidth(450);
 seriesGroup.setOverlap(-75);

 doc.save(getArtifactsDir() + "Charts.ConfigureGapOverlap.docx");
 
```

**Returns:**
int - النسبة المئوية لمقدار تداخل أشرطة أو أعمدة السلسلة.
### getSecondSectionSize() {#getSecondSectionSize}
```
public int getSecondSectionSize()
```


يحصل على حجم القسم الثانوي لمخطط الفطيرة كنسبة مئوية.

 **Remarks:** 

ينطبق على مجموعات السلاسل من الأنواع [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE) و[ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR).

النطاق المقبول للقيم هو من 5 إلى 200 شاملًا. القيمة الافتراضية هي 75.

 **Examples:** 

يعرض كيفية إنشاء وتنسيق مخطط فطيرة داخل فطيرة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.PIE_OF_PIE, 440.0, 300.0);
 Chart chart = shape.getChart();
 // Delete the default generated series.
 chart.getSeries().clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3", "Category 4" };
 chart.getSeries().add("Series 1", categories, new double[] { 11.0, 8.0, 4.0, 3.0 });

 // Format the Pie of Pie chart.
 ChartSeriesGroup seriesGroup = chart.getSeriesGroups().get(0);
 seriesGroup.setGapWidth(10);
 seriesGroup.setSecondSectionSize(77);

 doc.save(getArtifactsDir() + "Charts.PieOfPieChart.docx");
 
```

**Returns:**
int - حجم القسم الثانوي لمخطط الفطيرة كنسبة مئوية.
### getSeries() {#getSeries}
```
public ChartSeriesCollection getSeries()
```


يحصل على مجموعة من السلاسل التي تنتمي إلى مجموعة السلاسل هذه.

 **Examples:** 

يوضح كيفية العمل مع المحور الثانوي للمخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```

**Returns:**
[ChartSeriesCollection](../../com.aspose.words/chartseriescollection/) - A collection of series that belong to this series group.
### getSeriesType() {#getSeriesType}
```
public int getSeriesType()
```


يحصل على نوع سلاسل المخطط المتضمنة في هذه المجموعة.

 **Examples:** 

يوضح كيفية العمل مع المحور الثانوي للمخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```

**Returns:**
int - نوع سلسلة المخطط المتضمنة في هذه المجموعة. القيمة المرجعة هي واحدة من ثوابت [ChartSeriesType](../../com.aspose.words/chartseriestype/).
### setAxisGroup(int value) {#setAxisGroup-int}
```
public void setAxisGroup(int value)
```


يضبط مجموعة المحاور التي تنتمي إليها مجموعة السلاسل هذه.

 **Examples:** 

يوضح كيفية العمل مع المحور الثانوي للمخطط.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | مجموعة المحور التي تنتمي إليها مجموعة السلاسل هذه. يجب أن تكون القيمة واحدة من ثوابت [AxisGroup](../../com.aspose.words/axisgroup/). |

### setBubbleScale(int value) {#setBubbleScale-int}
```
public void setBubbleScale(int value)
```


يضبط حجم الفقاعات كنسبة مئوية من حجمها الافتراضي.

 **Remarks:** 

ينطبق فقط على مجموعات السلاسل من نوعي [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE) و [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D).

نطاق القيم المقبولة هو من 0 إلى 300 شاملًا. القيمة الافتراضية هي 100.

 **Examples:** 

عرض كيفية ضبط حجم الفقاعات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bubble 3D chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE_3_D, 450.0, 250.0);
 ChartSeriesGroup seriesGroup = shape.getChart().getSeriesGroups().get(0);

 // Set bubble scale to 200%.
 seriesGroup.setBubbleScale(200);

 doc.save(getArtifactsDir() + "Charts.BubbleScale.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | حجم الفقاعات كنسبة مئوية من حجمها الافتراضي. |

### setDoughnutHoleSize(int value) {#setDoughnutHoleSize-int}
```
public void setDoughnutHoleSize(int value)
```


يضبط حجم الفتحة في مخطط الدونات الأب كنسبة مئوية.

 **Remarks:** 

ينطبق فقط على مجموعات السلاسل من نوع [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT).

نطاق القيم المقبولة هو من 0 إلى 90 شاملًا. القيمة الافتراضية هي 75.

 **Examples:** 

يعرض كيفية إنشاء وتنسيق مخطط الدونات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.DOUGHNUT, 400.0, 400.0);
 Chart chart = shape.getChart();
 // Delete the default generated series.
 chart.getSeries().clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 chart.getSeries().add("Series 1", categories, new double[] { 4.0, 2.0, 5.0 });

 // Format the Doughnut chart.
 ChartSeriesGroup seriesGroup = chart.getSeriesGroups().get(0);
 seriesGroup.setDoughnutHoleSize(10);
 seriesGroup.setFirstSliceAngle(270);

 doc.save(getArtifactsDir() + "Charts.DoughnutChart.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | حجم الفتحة في مخطط الدونات الأصلي كنسبة مئوية. |

### setFirstSliceAngle(int value) {#setFirstSliceAngle-int}
```
public void setFirstSliceAngle(int value)
```


يضبط الزاوية، بالدرجات، للقطعة الأولى في مخطط الفطيرة الأب.

 **Remarks:** 

ينطبق على مجموعات السلاسل من الأنواع [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D) و[ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT) الأنواع.

النطاق المقبول للقيم هو من 0 إلى 360 شاملًا. القيمة الافتراضية هي 0.

 **Examples:** 

يعرض كيفية إنشاء وتنسيق مخطط الدونات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.DOUGHNUT, 400.0, 400.0);
 Chart chart = shape.getChart();
 // Delete the default generated series.
 chart.getSeries().clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 chart.getSeries().add("Series 1", categories, new double[] { 4.0, 2.0, 5.0 });

 // Format the Doughnut chart.
 ChartSeriesGroup seriesGroup = chart.getSeriesGroups().get(0);
 seriesGroup.setDoughnutHoleSize(10);
 seriesGroup.setFirstSliceAngle(270);

 doc.save(getArtifactsDir() + "Charts.DoughnutChart.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | الزاوية، بالدرجات، للقطاع الأول في مخطط الفطيرة الأصلي. |

### setGapWidth(int value) {#setGapWidth-int}
```
public void setGapWidth(int value)
```


يضبط نسبة عرض الفجوة بين عناصر المخطط.

 **Remarks:** 

ينطبق فقط على مجموعات السلاسل من أنواع الشريط، العمود، فطيرة-على-شريط، فطيرة-على-فطيرة، المخطط التكراري، الصندوق والشارب، الشلال والقمع.

النطاق المقبول للقيم هو من 0 إلى 500 شاملًا. بالنسبة لمجموعات السلاسل القائمة على الشريط/العمود، تمثل الخاصية المسافة بين مجموعات الأشرطة كنسبة مئوية من عرضها. بالنسبة لمخططات فطيرة-على-فطيرة وبار-على-فطيرة، هذه هي المسافة بين الأقسام الأساسية والثانوية للمخطط.

 **Examples:** 

يوضح كيفية ضبط عرض الفجوة والتداخل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 450.0, 250.0);
 ChartSeriesGroup seriesGroup = shape.getChart().getSeriesGroups().get(0);

 // Set column gap width and overlap.
 seriesGroup.setGapWidth(450);
 seriesGroup.setOverlap(-75);

 doc.save(getArtifactsDir() + "Charts.ConfigureGapOverlap.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | النسبة المئوية لعرض الفجوة بين عناصر المخطط. |

### setOverlap(int value) {#setOverlap-int}
```
public void setOverlap(int value)
```


يضبط النسبة المئوية لمدى تداخل أشرطة أو أعمدة السلسلة.

 **Remarks:** 

ينطبق على مجموعات السلاسل لجميع أنواع الشريط والعمود.

النطاق المقبول للقيم هو من -100 إلى 100 شاملًا. القيمة 0 تشير إلى عدم وجود مساحة بين الأشرطة/الأعمدة. إذا كانت القيمة -100، فإن المسافة بين الأشرطة/الأعمدة تساوي عرضها. القيمة 100 تعني أن الأشرطة/الأعمدة تتداخل تمامًا.

 **Examples:** 

يوضح كيفية ضبط عرض الفجوة والتداخل.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 450.0, 250.0);
 ChartSeriesGroup seriesGroup = shape.getChart().getSeriesGroups().get(0);

 // Set column gap width and overlap.
 seriesGroup.setGapWidth(450);
 seriesGroup.setOverlap(-75);

 doc.save(getArtifactsDir() + "Charts.ConfigureGapOverlap.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | النسبة المئوية لمقدار تداخل أشرطة أو أعمدة السلسلة. |

### setSecondSectionSize(int value) {#setSecondSectionSize-int}
```
public void setSecondSectionSize(int value)
```


يضبط حجم القسم الثانوي لمخطط الفطيرة كنسبة مئوية.

 **Remarks:** 

ينطبق على مجموعات السلاسل من الأنواع [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE) و[ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR).

النطاق المقبول للقيم هو من 5 إلى 200 شاملًا. القيمة الافتراضية هي 75.

 **Examples:** 

يعرض كيفية إنشاء وتنسيق مخطط فطيرة داخل فطيرة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.PIE_OF_PIE, 440.0, 300.0);
 Chart chart = shape.getChart();
 // Delete the default generated series.
 chart.getSeries().clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3", "Category 4" };
 chart.getSeries().add("Series 1", categories, new double[] { 11.0, 8.0, 4.0, 3.0 });

 // Format the Pie of Pie chart.
 ChartSeriesGroup seriesGroup = chart.getSeriesGroups().get(0);
 seriesGroup.setGapWidth(10);
 seriesGroup.setSecondSectionSize(77);

 doc.save(getArtifactsDir() + "Charts.PieOfPieChart.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | حجم القسم الثانوي لمخطط الفطيرة كنسبة مئوية. |

