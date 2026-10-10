---
title: "ChartSeriesGroup"
linktitle: "ChartSeriesGroup"
second_title: "Aspose.Words for Java"
description: "表示 chart series group 的属性，该属性是与相同坐标轴关联的相同类型 chart series 的属性（Java 中）。"
type: docs
weight: 87
url: /zh/java/com.aspose.words/chartseriesgroup/
---

**Inheritance:**
java.lang.Object
```
public class ChartSeriesGroup
```

表示 chart series group 的属性，即与相同坐标轴关联的相同类型 chart series 的属性。

 **Remarks:** 

组合图表包含多个 chart series group，每种系列类型对应一个单独的组。

此外，您可以创建 chart series group，以将次要坐标轴分配给一个或多个 chart series。

欲了解更多，请访问 [ Working with Charts ][Working with Charts] 文档文章。

 **Examples:** 

展示如何使用图表的次要坐标轴。

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
## 方法

| 方法 | 描述 |
| --- | --- |
| [getAxisGroup()](#getAxisGroup) | 获取此 series group 所属的轴组。 |
| [getAxisX()](#getAxisX) | 提供对该 series group 的 X 轴属性的访问。 |
| [getAxisY()](#getAxisY) | 提供对该 series group 的 Y 轴属性的访问。 |
| [getBubbleScale()](#getBubbleScale) | 获取气泡的大小，以其默认大小的百分比表示。 |
| [getDoughnutHoleSize()](#getDoughnutHoleSize) | 获取父环形图的孔大小，以百分比表示。 |
| [getFirstSliceAngle()](#getFirstSliceAngle) | 获取父饼图第一块的角度（以度为单位）。 |
| [getGapWidth()](#getGapWidth) | 获取图表元素之间间隙宽度的百分比。 |
| [getOverlap()](#getOverlap) | 获取系列条形或柱形重叠程度的百分比。 |
| [getSecondSectionSize()](#getSecondSectionSize) | 获取饼图次要部分的大小，以百分比表示。 |
| [getSeries()](#getSeries) | 获取属于此 series group 的系列集合。 |
| [getSeriesType()](#getSeriesType) | 获取此组中包含的 chart series 类型。 |
| [setAxisGroup(int value)](#setAxisGroup-int) | 设置此 series group 所属的轴组。 |
| [setBubbleScale(int value)](#setBubbleScale-int) | 设置气泡的大小，以其默认大小的百分比表示。 |
| [setDoughnutHoleSize(int value)](#setDoughnutHoleSize-int) | 设置父环形图的孔大小，以百分比表示。 |
| [setFirstSliceAngle(int value)](#setFirstSliceAngle-int) | 设置父饼图第一块的角度（以度为单位）。 |
| [setGapWidth(int value)](#setGapWidth-int) | 设置图表元素之间间隙宽度的百分比。 |
| [setOverlap(int value)](#setOverlap-int) | 设置系列条形或柱形重叠程度的百分比。 |
| [setSecondSectionSize(int value)](#setSecondSectionSize-int) | 设置饼图次要部分的大小，以百分比表示。 |
### getAxisGroup() {#getAxisGroup}
```
public int getAxisGroup()
```


获取此 series group 所属的轴组。

 **Examples:** 

展示如何使用图表的次要坐标轴。

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
int - 此系列组所属的坐标轴组。返回值是 [AxisGroup](../../com.aspose.words/axisgroup/) 常量之一。
### getAxisX() {#getAxisX}
```
public ChartAxis getAxisX()
```


提供对该 series group 的 X 轴属性的访问。

 **Examples:** 

展示如何使用图表的次要坐标轴。

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


提供对该 series group 的 Y 轴属性的访问。

 **Examples:** 

展示如何使用图表的次要坐标轴。

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


获取气泡的大小，以其默认大小的百分比表示。

 **Remarks:** 

仅适用于 [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE) 和 [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D) 类型的系列组。

可接受值的范围为 0 到 300（含）。默认值为 100。

 **Examples:** 

展示如何设置气泡的大小。

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
int - 气泡大小，以其默认大小的百分比表示。
### getDoughnutHoleSize() {#getDoughnutHoleSize}
```
public int getDoughnutHoleSize()
```


获取父环形图的孔大小，以百分比表示。

 **Remarks:** 

仅适用于 [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT) 类型的系列组。

可接受值的范围为 0 到 90（含）。默认值为 75。

 **Examples:** 

展示如何创建和格式化环形图。

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
int - 父环形图的孔大小，以百分比表示。
### getFirstSliceAngle() {#getFirstSliceAngle}
```
public int getFirstSliceAngle()
```


获取父饼图第一块的角度（以度为单位）。

 **Remarks:** 

适用于 [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D) 和 [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT) 类型的系列组。

可接受值的范围为 0 到 360（含）。默认值为 0。

 **Examples:** 

展示如何创建和格式化环形图。

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
int - 父饼图第一块切片的角度（以度为单位）。
### getGapWidth() {#getGapWidth}
```
public int getGapWidth()
```


获取图表元素之间间隙宽度的百分比。

 **Remarks:** 

仅适用于条形图、柱形图、饼图-条形图、饼图-饼图、直方图、箱线图、瀑布图和漏斗图类型的系列组。

可接受值的范围为 0 到 500（含）。对于基于条形/柱形的系列组，此属性表示条形簇之间的间距，以其宽度的百分比表示。对于饼图-饼图和条形-饼图图表，则表示主次部分之间的间距。

 **Examples:** 

展示如何配置间隙宽度和重叠。

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
int - 图表元素之间间隙宽度的百分比。
### getOverlap() {#getOverlap}
```
public int getOverlap()
```


获取系列条形或柱形重叠程度的百分比。

 **Remarks:** 

适用于所有条形和柱形类型的系列组。

可接受值的范围为 -100 到 100（含）。值为 0 表示条形/柱形之间没有间距。若值为 -100，则条形/柱形之间的距离等于它们的宽度。值为 100 表示条形/柱形完全重叠。

 **Examples:** 

展示如何配置间隙宽度和重叠。

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
int - 系列条形或柱形重叠程度的百分比。
### getSecondSectionSize() {#getSecondSectionSize}
```
public int getSecondSectionSize()
```


获取饼图次要部分的大小，以百分比表示。

 **Remarks:** 

适用于 [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE) 和 [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR) 类型的系列组。

可接受值的范围为 5 到 200（含）。默认值为 75。

 **Examples:** 

展示如何创建和格式化饼图-饼图。

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
int - 饼图次要部分的大小，以百分比表示。
### getSeries() {#getSeries}
```
public ChartSeriesCollection getSeries()
```


获取属于此 series group 的系列集合。

 **Examples:** 

展示如何使用图表的次要坐标轴。

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


获取此组中包含的 chart series 类型。

 **Examples:** 

展示如何使用图表的次要坐标轴。

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
int - 此组中包含的图表系列类型。返回值是 [ChartSeriesType](../../com.aspose.words/chartseriestype/) 常量之一。
### setAxisGroup(int value) {#setAxisGroup-int}
```
public void setAxisGroup(int value)
```


设置此 series group 所属的轴组。

 **Examples:** 

展示如何使用图表的次要坐标轴。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 此系列组所属的坐标轴组。该值必须是 [AxisGroup](../../com.aspose.words/axisgroup/) 常量之一。 |

### setBubbleScale(int value) {#setBubbleScale-int}
```
public void setBubbleScale(int value)
```


设置气泡的大小，以其默认大小的百分比表示。

 **Remarks:** 

仅适用于 [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE) 和 [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D) 类型的系列组。

可接受值的范围为 0 到 300（含）。默认值为 100。

 **Examples:** 

展示如何设置气泡的大小。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 气泡的大小占其默认大小的百分比。 |

### setDoughnutHoleSize(int value) {#setDoughnutHoleSize-int}
```
public void setDoughnutHoleSize(int value)
```


设置父环形图的孔大小，以百分比表示。

 **Remarks:** 

仅适用于 [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT) 类型的系列组。

可接受值的范围为 0 到 90（含）。默认值为 75。

 **Examples:** 

展示如何创建和格式化环形图。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 父环形图的孔大小的百分比。 |

### setFirstSliceAngle(int value) {#setFirstSliceAngle-int}
```
public void setFirstSliceAngle(int value)
```


设置父饼图第一块的角度（以度为单位）。

 **Remarks:** 

适用于 [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D) 和 [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT) 类型的系列组。

可接受值的范围为 0 到 360（含）。默认值为 0。

 **Examples:** 

展示如何创建和格式化环形图。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 父饼图第一块的角度（以度为单位）。 |

### setGapWidth(int value) {#setGapWidth-int}
```
public void setGapWidth(int value)
```


设置图表元素之间间隙宽度的百分比。

 **Remarks:** 

仅适用于条形图、柱形图、饼图-条形图、饼图-饼图、直方图、箱线图、瀑布图和漏斗图类型的系列组。

可接受值的范围为 0 到 500（含）。对于基于条形/柱形的系列组，此属性表示条形簇之间的间距，以其宽度的百分比表示。对于饼图-饼图和条形-饼图图表，则表示主次部分之间的间距。

 **Examples:** 

展示如何配置间隙宽度和重叠。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 图表元素之间间隙宽度的百分比。 |

### setOverlap(int value) {#setOverlap-int}
```
public void setOverlap(int value)
```


设置系列条形或柱形重叠程度的百分比。

 **Remarks:** 

适用于所有条形和柱形类型的系列组。

可接受值的范围为 -100 到 100（含）。值为 0 表示条形/柱形之间没有间距。若值为 -100，则条形/柱形之间的距离等于它们的宽度。值为 100 表示条形/柱形完全重叠。

 **Examples:** 

展示如何配置间隙宽度和重叠。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 系列柱或列重叠程度的百分比。 |

### setSecondSectionSize(int value) {#setSecondSectionSize-int}
```
public void setSecondSectionSize(int value)
```


设置饼图次要部分的大小，以百分比表示。

 **Remarks:** 

适用于 [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE) 和 [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR) 类型的系列组。

可接受值的范围为 5 到 200（含）。默认值为 75。

 **Examples:** 

展示如何创建和格式化饼图-饼图。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 饼图次要部分的大小占比。 |

