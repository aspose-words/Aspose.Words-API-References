---
title: "ChartDataLabelCollection"
linktitle: "ChartDataLabelCollection"
second_title: "Aspose.Words для Java"
description: "Представляет собой коллекцию объектов ChartDataLabel в Java."
type: docs
weight: 72
url: /ru/java/com.aspose.words/chartdatalabelcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartDataLabelCollection implements Iterable
```

Представляет собой коллекцию [ChartDataLabel](../../com.aspose.words/chartdatalabel/).

Чтобы узнать больше, посетите статью документации [ Working with Charts ][Working with Charts].

 **Examples:** 

Показывает, как применять подписи к точкам данных в линейной диаграмме.

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
## Методы

| Метод | Описание |
| --- | --- |
| [clearFormat()](#clearFormat) | Очищает формат всех [ChartDataLabel](../../com.aspose.words/chartdatalabel/) в этой коллекции. |
| [get(int index)](#get-int) | Возвращает [ChartDataLabel](../../com.aspose.words/chartdatalabel/) для указанного индекса. |
| [getCount()](#getCount) | Возвращает количество [ChartDataLabel](../../com.aspose.words/chartdatalabel/) в этой коллекции. |
| [getFont()](#getFont) | Обеспечивает доступ к форматированию шрифта подписей данных всей серии. |
| [getFormat()](#getFormat) | Обеспечивает доступ к заполнению и форматированию линий подписей данных. |
| [getNumberFormat()](#getNumberFormat) | Получает экземпляр [ChartNumberFormat](../../com.aspose.words/chartnumberformat/), позволяющий задать числовой формат для подписей данных всей серии. |
| [getOrientation()](#getOrientation) | Получает ориентацию текста подписей данных всей серии. |
| [getPosition()](#getPosition) | Получает позицию подписей данных. |
| [getRotation()](#getRotation) | Получает вращение подписей данных всей серии в градусах. |
| [getSeparator()](#getSeparator) | Получает строковый разделитель, используемый для подписей данных всей серии. |
| [getShapeType()](#getShapeType) |  |
| [getShowBubbleSize()](#getShowBubbleSize) | Позволяет указать, следует ли отображать размер пузыря для подписей данных всей серии. |
| [getShowCategoryName()](#getShowCategoryName) | Позволяет указать, следует ли отображать название категории для подписей данных всей серии. |
| [getShowDataLabelsRange()](#getShowDataLabelsRange) | Позволяет указать, следует ли отображать значения из диапазона подписей данных в подписях всей серии. |
| [getShowLeaderLines()](#getShowLeaderLines) | Позволяет указать, следует ли показывать линии-указатели подписей данных для всей серии. |
| [getShowLegendKey()](#getShowLegendKey) | Позволяет указать, следует ли отображать ключ легенды для подписей данных всей серии. |
| [getShowPercentage()](#getShowPercentage) | Позволяет указать, следует ли отображать процентное значение для подписей данных всей серии. |
| [getShowSeriesName()](#getShowSeriesName) | Получает логическое значение, указывающее поведение отображения имени серии для подписей данных всей серии. |
| [getShowValue()](#getShowValue) | Позволяет указать, следует ли отображать значения в подписях данных всей серии. |
| [isFillSupported()](#isFillSupported) |  |
| [isFormatDefined()](#isFormatDefined) |  |
| [isInherited()](#isInherited) |  |
| [iterator()](#iterator) | Возвращает объект перечислителя. |
| [materializeSpPr()](#materializeSpPr) |  |
| [setOrientation(int value)](#setOrientation-int) | Устанавливает ориентацию текста меток данных всей серии. |
| [setPosition(int value)](#setPosition-int) | Устанавливает положение меток данных. |
| [setRotation(int value)](#setRotation-int) | Устанавливает вращение меток данных всей серии в градусах. |
| [setSeparator(String value)](#setSeparator-java.lang.String) | Устанавливает строковый разделитель, используемый для меток данных всей серии. |
| [setShapeType(int value)](#setShapeType-int) |  |
| [setShowBubbleSize(boolean value)](#setShowBubbleSize-boolean) | Позволяет указать, следует ли отображать размер пузыря для подписей данных всей серии. |
| [setShowCategoryName(boolean value)](#setShowCategoryName-boolean) | Позволяет указать, следует ли отображать название категории для подписей данных всей серии. |
| [setShowDataLabelsRange(boolean value)](#setShowDataLabelsRange-boolean) | Позволяет указать, следует ли отображать значения из диапазона подписей данных в подписях всей серии. |
| [setShowLeaderLines(boolean value)](#setShowLeaderLines-boolean) | Позволяет указать, следует ли показывать линии-указатели подписей данных для всей серии. |
| [setShowLegendKey(boolean value)](#setShowLegendKey-boolean) | Позволяет указать, следует ли отображать ключ легенды для подписей данных всей серии. |
| [setShowPercentage(boolean value)](#setShowPercentage-boolean) | Позволяет указать, следует ли отображать процентное значение для подписей данных всей серии. |
| [setShowSeriesName(boolean value)](#setShowSeriesName-boolean) | Устанавливает логическое значение, указывающее поведение отображения имени серии для меток данных всей серии. |
| [setShowValue(boolean value)](#setShowValue-boolean) | Позволяет указать, следует ли отображать значения в подписях данных всей серии. |
### clearFormat() {#clearFormat}
```
public void clearFormat()
```


Очищает формат всех [ChartDataLabel](../../com.aspose.words/chartdatalabel/) в этой коллекции.

 **Examples:** 

Показывает, как применять подписи к точкам данных в линейной диаграмме.

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


Возвращает [ChartDataLabel](../../com.aspose.words/chartdatalabel/) для указанного индекса.

 **Examples:** 

Показывает, как применять подписи к точкам данных в линейной диаграмме.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int |  |

**Returns:**
[ChartDataLabel](../../com.aspose.words/chartdatalabel/) - [ChartDataLabel](../../com.aspose.words/chartdatalabel/) for the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Возвращает количество [ChartDataLabel](../../com.aspose.words/chartdatalabel/) в этой коллекции.

 **Examples:** 

Показывает, как применять подписи к точкам данных в линейной диаграмме.

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
int - Количество [ChartDataLabel](../../com.aspose.words/chartdatalabel/) в этой коллекции.
### getFont() {#getFont}
```
public Font getFont()
```


Обеспечивает доступ к форматированию шрифта подписей данных всей серии.

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной метки данных с помощью свойства [ChartDataLabel.getFont()](../../com.aspose.words/chartdatalabel/\#getFont).

 **Examples:** 

Показывает, как включить и настроить метки данных для серии диаграммы.

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


Обеспечивает доступ к заполнению и форматированию линий подписей данных.

 **Examples:** 

Показывает, как задать заполнение, обводку и форматирование выноски для меток данных диаграммы.

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


Получает экземпляр [ChartNumberFormat](../../com.aspose.words/chartnumberformat/), позволяющий задать числовой формат для подписей данных всей серии.

 **Examples:** 

Показывает, как включить и настроить метки данных для серии диаграммы.

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


Получает ориентацию текста подписей данных всей серии.

 **Remarks:** 

Значение по умолчанию — [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL).

 **Examples:** 

Показывает, как изменить ориентацию и вращение меток данных.

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
int - Ориентация текста меток данных всей серии. Возвращаемое значение является одной из констант [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/).
### getPosition() {#getPosition}
```
public int getPosition()
```


Получает позицию подписей данных.

 **Remarks:** 

Позицию можно установить для меток данных следующих типов серий диаграмм:

\- [ChartSeriesType.BAR](../../com.aspose.words/chartseriestype/\#BAR), [ChartSeriesType.COLUMN](../../com.aspose.words/chartseriestype/\#COLUMN), [ChartSeriesType.HISTOGRAM](../../com.aspose.words/chartseriestype/\#HISTOGRAM), [ChartSeriesType.PARETO](../../com.aspose.words/chartseriestype/\#PARETO), [ChartSeriesType.WATERFALL](../../com.aspose.words/chartseriestype/\#WATERFALL); разрешённые значения: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END) и [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END);

\- [ChartSeriesType.BAR\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-STACKED), [ChartSeriesType.BAR\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-PERCENT-STACKED), [ChartSeriesType.COLUMN\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-STACKED), [ChartSeriesType.COLUMN\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-PERCENT-STACKED); разрешённые значения: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE) и [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END);

\- [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE), [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D), [ChartSeriesType.LINE](../../com.aspose.words/chartseriestype/\#LINE), [ChartSeriesType.LINE\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-STACKED), [ChartSeriesType.LINE\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-PERCENT-STACKED), [ChartSeriesType.SCATTER](../../com.aspose.words/chartseriestype/\#SCATTER), [ChartSeriesType.STOCK](../../com.aspose.words/chartseriestype/\#STOCK); разрешённые значения: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) и [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW);

\- [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D), [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR), [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE); допустимые значения: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END), [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END) и [ChartDataLabelPosition.BEST\_FIT](../../com.aspose.words/chartdatalabelposition/\#BEST-FIT);

\- [ChartSeriesType.BOX\_AND\_WHISKER](../../com.aspose.words/chartseriestype/\#BOX-AND-WHISKER); допустимые значения: [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) и [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW).

 **Examples:** 

Показывает, как установить позицию подписи данных.

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
int - Позиция подписей данных. Возвращаемое значение — одна из констант [ChartDataLabelPosition](../../com.aspose.words/chartdatalabelposition/).
### getRotation() {#getRotation}
```
public int getRotation()
```


Получает вращение подписей данных всей серии в градусах.

 **Remarks:** 

Диапазон допустимых значений от -180 до 180 включительно. Значение по умолчанию — 0.

Если значение [getOrientation()](../../com.aspose.words/chartdatalabelcollection/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/chartdatalabelcollection/\#setOrientation-int) равно [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL), формы подписей, если они существуют, вращаются вместе с текстом подписи. В противном случае вращается только текст подписи.

 **Examples:** 

Показывает, как изменить ориентацию и вращение меток данных.

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
int - Поворот подписей данных всей серии в градусах.
### getSeparator() {#getSeparator}
```
public String getSeparator()
```


Получает строковый разделитель, используемый для подписей данных всей серии. По умолчанию это запятая, за исключением круговых диаграмм, отображающих только название категории и процент, где вместо этого используется разрыв строки.

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной подписи данных с помощью свойства [ChartDataLabel.getSeparator()](../../com.aspose.words/chartdatalabel/\#getSeparator) / [ChartDataLabel.setSeparator(java.lang.String)](../../com.aspose.words/chartdatalabel/\#setSeparator-java.lang.String).

 **Examples:** 

Показывает, как работать с подписями данных пузырьковой диаграммы.

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

Показывает, как работать с подписями данных круговой диаграммы.

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
java.lang.String - Строковый разделитель, используемый для подписей данных всей серии.
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


Позволяет указать, следует ли отображать размер пузыря в подписях данных всей серии. Применяется только к пузырьковым диаграммам. Значение по умолчанию — false.

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной подписи данных с помощью свойства [ChartDataLabel.getShowBubbleSize()](../../com.aspose.words/chartdatalabel/\#getShowBubbleSize) / [ChartDataLabel.setShowBubbleSize(boolean)](../../com.aspose.words/chartdatalabel/\#setShowBubbleSize-boolean).

 **Examples:** 

Показывает, как работать с подписями данных пузырьковой диаграммы.

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
boolean - Соответствующее  boolean  значение.
### getShowCategoryName() {#getShowCategoryName}
```
public boolean getShowCategoryName()
```


Позволяет указать, следует ли отображать название категории в подписях данных всей серии. Значение по умолчанию — false.

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной подписи данных с помощью свойства [ChartDataLabel.getShowCategoryName()](../../com.aspose.words/chartdatalabel/\#getShowCategoryName) / [ChartDataLabel.setShowCategoryName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowCategoryName-boolean).

 **Examples:** 

Показывает, как работать с подписями данных пузырьковой диаграммы.

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
boolean - Соответствующее  boolean  значение.
### getShowDataLabelsRange() {#getShowDataLabelsRange}
```
public boolean getShowDataLabelsRange()
```


Позволяет указать, следует ли отображать значения из диапазона подписей данных в подписях данных всей серии. Значение по умолчанию — false.

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной подписи данных с помощью свойства [ChartDataLabel.getShowDataLabelsRange()](../../com.aspose.words/chartdatalabel/\#getShowDataLabelsRange) / [ChartDataLabel.setShowDataLabelsRange(boolean)](../../com.aspose.words/chartdatalabel/\#setShowDataLabelsRange-boolean).

 **Examples:** 

Показывает, как применять подписи к точкам данных в линейной диаграмме.

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
boolean - Соответствующее  boolean  значение.
### getShowLeaderLines() {#getShowLeaderLines}
```
public boolean getShowLeaderLines()
```


Позволяет указать, следует ли отображать линии‑выноски меток данных для меток данных всей серии. Значение по умолчанию — false.

 **Remarks:** 

Применяется только к круговым диаграммам. Линии‑выноски создают визуальную связь между меткой данных и соответствующей точкой данных.

Значение, определённое для этого свойства, может быть переопределено для отдельной метки данных с использованием свойства [ChartDataLabel.getShowLeaderLines()](../../com.aspose.words/chartdatalabel/\#getShowLeaderLines) / [ChartDataLabel.setShowLeaderLines(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLeaderLines-boolean).

 **Examples:** 

Показывает, как работать с подписями данных круговой диаграммы.

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
boolean - Соответствующее  boolean  значение.
### getShowLegendKey() {#getShowLegendKey}
```
public boolean getShowLegendKey()
```


Позволяет указать, следует ли отображать ключ легенды для меток данных всей серии. Значение по умолчанию — false.

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной метки данных с использованием свойства [ChartDataLabel.getShowLegendKey()](../../com.aspose.words/chartdatalabel/\#getShowLegendKey) / [ChartDataLabel.setShowLegendKey(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLegendKey-boolean).

 **Examples:** 

Показывает, как работать с подписями данных круговой диаграммы.

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
boolean - Соответствующее  boolean  значение.
### getShowPercentage() {#getShowPercentage}
```
public boolean getShowPercentage()
```


Позволяет указать, следует ли отображать процентное значение для меток данных всей серии. Значение по умолчанию — false. Применяется только к круговым диаграммам.

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной метки данных с использованием свойства [ChartDataLabel.getShowPercentage()](../../com.aspose.words/chartdatalabel/\#getShowPercentage) / [ChartDataLabel.setShowPercentage(boolean)](../../com.aspose.words/chartdatalabel/\#setShowPercentage-boolean).

 **Examples:** 

Показывает, как работать с подписями данных круговой диаграммы.

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
boolean - Соответствующее  boolean  значение.
### getShowSeriesName() {#getShowSeriesName}
```
public boolean getShowSeriesName()
```


Возвращает Boolean, указывающий поведение отображения имени серии для меток данных всей серии.  true  — показать имя серии;  false  — скрыть. По умолчанию  false .

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной метки данных с использованием свойства [ChartDataLabel.getShowSeriesName()](../../com.aspose.words/chartdatalabel/\#getShowSeriesName) / [ChartDataLabel.setShowSeriesName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowSeriesName-boolean).

 **Examples:** 

Показывает, как работать с подписями данных пузырьковой диаграммы.

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
boolean — Boolean, указывающий поведение отображения имени серии для меток данных всей серии.
### getShowValue() {#getShowValue}
```
public boolean getShowValue()
```


Позволяет указать, следует ли отображать значения в метках данных всей серии. Значение по умолчанию — false.

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной метки данных с использованием свойства [ChartDataLabel.getShowValue()](../../com.aspose.words/chartdatalabel/\#getShowValue) / [ChartDataLabel.setShowValue(boolean)](../../com.aspose.words/chartdatalabel/\#setShowValue-boolean).

 **Examples:** 

Показывает, как работать с подписями данных круговой диаграммы.

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
boolean - Соответствующее  boolean  значение.
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


Возвращает объект перечислителя.

 **Examples:** 

Показывает, как применять подписи к точкам данных в линейной диаграмме.

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


Устанавливает ориентацию текста меток данных всей серии.

 **Remarks:** 

Значение по умолчанию — [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL).

 **Examples:** 

Показывает, как изменить ориентацию и вращение меток данных.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Ориентация текста меток данных всей серии. Значение должно быть одной из констант [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/). |

### setPosition(int value) {#setPosition-int}
```
public void setPosition(int value)
```


Устанавливает положение меток данных.

 **Remarks:** 

Позицию можно установить для меток данных следующих типов серий диаграмм:

\- [ChartSeriesType.BAR](../../com.aspose.words/chartseriestype/\#BAR), [ChartSeriesType.COLUMN](../../com.aspose.words/chartseriestype/\#COLUMN), [ChartSeriesType.HISTOGRAM](../../com.aspose.words/chartseriestype/\#HISTOGRAM), [ChartSeriesType.PARETO](../../com.aspose.words/chartseriestype/\#PARETO), [ChartSeriesType.WATERFALL](../../com.aspose.words/chartseriestype/\#WATERFALL); разрешённые значения: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END) и [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END);

\- [ChartSeriesType.BAR\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-STACKED), [ChartSeriesType.BAR\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-PERCENT-STACKED), [ChartSeriesType.COLUMN\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-STACKED), [ChartSeriesType.COLUMN\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-PERCENT-STACKED); разрешённые значения: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE) и [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END);

\- [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE), [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D), [ChartSeriesType.LINE](../../com.aspose.words/chartseriestype/\#LINE), [ChartSeriesType.LINE\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-STACKED), [ChartSeriesType.LINE\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-PERCENT-STACKED), [ChartSeriesType.SCATTER](../../com.aspose.words/chartseriestype/\#SCATTER), [ChartSeriesType.STOCK](../../com.aspose.words/chartseriestype/\#STOCK); разрешённые значения: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) и [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW);

\- [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D), [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR), [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE); допустимые значения: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END), [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END) и [ChartDataLabelPosition.BEST\_FIT](../../com.aspose.words/chartdatalabelposition/\#BEST-FIT);

\- [ChartSeriesType.BOX\_AND\_WHISKER](../../com.aspose.words/chartseriestype/\#BOX-AND-WHISKER); допустимые значения: [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) и [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW).

 **Examples:** 

Показывает, как установить позицию подписи данных.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Позиция меток данных. Значение должно быть одной из констант [ChartDataLabelPosition](../../com.aspose.words/chartdatalabelposition/). |

### setRotation(int value) {#setRotation-int}
```
public void setRotation(int value)
```


Устанавливает вращение меток данных всей серии в градусах.

 **Remarks:** 

Диапазон допустимых значений от -180 до 180 включительно. Значение по умолчанию — 0.

Если значение [getOrientation()](../../com.aspose.words/chartdatalabelcollection/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/chartdatalabelcollection/\#setOrientation-int) равно [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL), формы подписей, если они существуют, вращаются вместе с текстом подписи. В противном случае вращается только текст подписи.

 **Examples:** 

Показывает, как изменить ориентацию и вращение меток данных.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Поворот меток данных всей серии в градусах. |

### setSeparator(String value) {#setSeparator-java.lang.String}
```
public void setSeparator(String value)
```


Устанавливает строковый разделитель, используемый для меток данных всей серии. По умолчанию — запятая, за исключением круговых диаграмм, показывающих только название категории и процент, где вместо неё используется разрыв строки.

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной подписи данных с помощью свойства [ChartDataLabel.getSeparator()](../../com.aspose.words/chartdatalabel/\#getSeparator) / [ChartDataLabel.setSeparator(java.lang.String)](../../com.aspose.words/chartdatalabel/\#setSeparator-java.lang.String).

 **Examples:** 

Показывает, как работать с подписями данных пузырьковой диаграммы.

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

Показывает, как работать с подписями данных круговой диаграммы.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Строковый разделитель, используемый для меток данных всей серии. |

### setShapeType(int value) {#setShapeType-int}
```
public void setShapeType(int value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int |  |

### setShowBubbleSize(boolean value) {#setShowBubbleSize-boolean}
```
public void setShowBubbleSize(boolean value)
```


Позволяет указать, следует ли отображать размер пузыря в подписях данных всей серии. Применяется только к пузырьковым диаграммам. Значение по умолчанию — false.

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной подписи данных с помощью свойства [ChartDataLabel.getShowBubbleSize()](../../com.aspose.words/chartdatalabel/\#getShowBubbleSize) / [ChartDataLabel.setShowBubbleSize(boolean)](../../com.aspose.words/chartdatalabel/\#setShowBubbleSize-boolean).

 **Examples:** 

Показывает, как работать с подписями данных пузырьковой диаграммы.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setShowCategoryName(boolean value) {#setShowCategoryName-boolean}
```
public void setShowCategoryName(boolean value)
```


Позволяет указать, следует ли отображать название категории в подписях данных всей серии. Значение по умолчанию — false.

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной подписи данных с помощью свойства [ChartDataLabel.getShowCategoryName()](../../com.aspose.words/chartdatalabel/\#getShowCategoryName) / [ChartDataLabel.setShowCategoryName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowCategoryName-boolean).

 **Examples:** 

Показывает, как работать с подписями данных пузырьковой диаграммы.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setShowDataLabelsRange(boolean value) {#setShowDataLabelsRange-boolean}
```
public void setShowDataLabelsRange(boolean value)
```


Позволяет указать, следует ли отображать значения из диапазона подписей данных в подписях данных всей серии. Значение по умолчанию — false.

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной подписи данных с помощью свойства [ChartDataLabel.getShowDataLabelsRange()](../../com.aspose.words/chartdatalabel/\#getShowDataLabelsRange) / [ChartDataLabel.setShowDataLabelsRange(boolean)](../../com.aspose.words/chartdatalabel/\#setShowDataLabelsRange-boolean).

 **Examples:** 

Показывает, как применять подписи к точкам данных в линейной диаграмме.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setShowLeaderLines(boolean value) {#setShowLeaderLines-boolean}
```
public void setShowLeaderLines(boolean value)
```


Позволяет указать, следует ли отображать линии‑выноски меток данных для меток данных всей серии. Значение по умолчанию — false.

 **Remarks:** 

Применяется только к круговым диаграммам. Линии‑выноски создают визуальную связь между меткой данных и соответствующей точкой данных.

Значение, определённое для этого свойства, может быть переопределено для отдельной метки данных с использованием свойства [ChartDataLabel.getShowLeaderLines()](../../com.aspose.words/chartdatalabel/\#getShowLeaderLines) / [ChartDataLabel.setShowLeaderLines(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLeaderLines-boolean).

 **Examples:** 

Показывает, как работать с подписями данных круговой диаграммы.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setShowLegendKey(boolean value) {#setShowLegendKey-boolean}
```
public void setShowLegendKey(boolean value)
```


Позволяет указать, следует ли отображать ключ легенды для меток данных всей серии. Значение по умолчанию — false.

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной метки данных с использованием свойства [ChartDataLabel.getShowLegendKey()](../../com.aspose.words/chartdatalabel/\#getShowLegendKey) / [ChartDataLabel.setShowLegendKey(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLegendKey-boolean).

 **Examples:** 

Показывает, как работать с подписями данных круговой диаграммы.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setShowPercentage(boolean value) {#setShowPercentage-boolean}
```
public void setShowPercentage(boolean value)
```


Позволяет указать, следует ли отображать процентное значение для меток данных всей серии. Значение по умолчанию — false. Применяется только к круговым диаграммам.

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной метки данных с использованием свойства [ChartDataLabel.getShowPercentage()](../../com.aspose.words/chartdatalabel/\#getShowPercentage) / [ChartDataLabel.setShowPercentage(boolean)](../../com.aspose.words/chartdatalabel/\#setShowPercentage-boolean).

 **Examples:** 

Показывает, как работать с подписями данных круговой диаграммы.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setShowSeriesName(boolean value) {#setShowSeriesName-boolean}
```
public void setShowSeriesName(boolean value)
```


Устанавливает Boolean, указывающий поведение отображения имени серии для меток данных всей серии.  true  — показать имя серии;  false  — скрыть. По умолчанию  false .

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной метки данных с использованием свойства [ChartDataLabel.getShowSeriesName()](../../com.aspose.words/chartdatalabel/\#getShowSeriesName) / [ChartDataLabel.setShowSeriesName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowSeriesName-boolean).

 **Examples:** 

Показывает, как работать с подписями данных пузырьковой диаграммы.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Boolean, указывающий поведение отображения имени серии для меток данных всей серии. |

### setShowValue(boolean value) {#setShowValue-boolean}
```
public void setShowValue(boolean value)
```


Позволяет указать, следует ли отображать значения в метках данных всей серии. Значение по умолчанию — false.

 **Remarks:** 

Значение, определённое для этого свойства, может быть переопределено для отдельной метки данных с использованием свойства [ChartDataLabel.getShowValue()](../../com.aspose.words/chartdatalabel/\#getShowValue) / [ChartDataLabel.setShowValue(boolean)](../../com.aspose.words/chartdatalabel/\#setShowValue-boolean).

 **Examples:** 

Показывает, как работать с подписями данных круговой диаграммы.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

