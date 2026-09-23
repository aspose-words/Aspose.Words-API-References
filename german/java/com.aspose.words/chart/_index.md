---
title: "Diagramm"
linktitle: "Diagramm"
second_title: "Aspose.Words für Java"
description: "Stellt Zugriff auf die Diagramm‑Formeigenschaften in Java bereit."
type: docs
weight: 66
url: /de/java/com.aspose.words/chart/
---

**Inheritance:**
java.lang.Object
```
public class Chart
```

Stellt Zugriff auf die Eigenschaften der Diagrammform bereit.

Weitere Informationen finden Sie im Dokumentationsartikel zu [ Working with Charts ][Working with Charts].

 **Examples:** 

Zeigt, wie man ein Diagramm einfügt und einen Titel festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a chart shape with a document builder and get its chart.
 Shape chartShape = builder.insertChart(ChartType.BAR, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Use the "Title" property to give our chart a title, which appears at the top center of the chart area.
 ChartTitle title = chart.getTitle();
 title.setText("My Chart");
 title.getFont().setSize(15.0);
 title.getFont().setColor(Color.BLUE);

 // Set the "Show" property to "true" to make the title visible.
 title.setShow(true);

 // Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
 title.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartTitle.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getAxes()](#getAxes) | Ruft eine Sammlung aller Achsen dieses Diagramms ab. |
| [getAxisX()](#getAxisX) | Stellt Zugriff auf die Eigenschaften der primären X‑Achse des Diagramms bereit. |
| [getAxisY()](#getAxisY) | Stellt Zugriff auf die Eigenschaften der primären Y‑Achse des Diagramms bereit. |
| [getAxisZ()](#getAxisZ) | Stellt Zugriff auf die Eigenschaften der Z‑Achse des Diagramms bereit. |
| [getDataTable()](#getDataTable) | Stellt Zugriff auf die Eigenschaften einer Datentabelle dieses Diagramms bereit. |
| [getFormat()](#getFormat) | Stellt Zugriff auf Füll‑ und Linienformatierung des Diagramms bereit. |
| [getLegend()](#getLegend) | Stellt Zugriff auf die Eigenschaften der Diagrammlegende bereit. |
| [getSeries()](#getSeries) | Stellt Zugriff auf die Serien‑Sammlung bereit. |
| [getSeriesGroups()](#getSeriesGroups) | Stellt Zugriff auf eine Seriengruppen‑Sammlung dieses Diagramms bereit. |
| [getShapeType()](#getShapeType) |  |
| [getSourceFullName()](#getSourceFullName) | Ermittelt den Pfad und Namen einer xls/xlsx‑Datei, mit der dieses Diagramm verknüpft ist. |
| [getStyle()](#getStyle) | Ermittelt den Stil des Diagramms. |
| [getTitle()](#getTitle) | Stellt Zugriff auf die Eigenschaften des Diagrammtitels bereit. |
| [isFillSupported()](#isFillSupported) |  |
| [isFormatDefined()](#isFormatDefined) |  |
| [materializeSpPr()](#materializeSpPr) |  |
| [setShapeType(int value)](#setShapeType-int) |  |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String) | Ermittelt den Pfad und Namen einer xls/xlsx‑Datei, mit der dieses Diagramm verknüpft ist. |
| [setStyle(int value)](#setStyle-int) | Legt den Stil des Diagramms fest. |
### getAxes() {#getAxes}
```
public ChartAxisCollection getAxes()
```


Ruft eine Sammlung aller Achsen dieses Diagramms ab.

 **Examples:** 

Zeigt, wie mit einer Achsensammlung gearbeitet wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Hide the major grid lines on the primary and secondary Y axes.
 for (ChartAxis axis : chart.getAxes())
 {
     if (axis.getType() == ChartAxisType.VALUE)
         axis.hasMajorGridlines(false);
 }

 doc.save(getArtifactsDir() + "Charts.AxisCollection.docx");
 
```

**Returns:**
[ChartAxisCollection](../../com.aspose.words/chartaxiscollection/) - A collection of all axes of this chart.
### getAxisX() {#getAxisX}
```
public ChartAxis getAxisX()
```


Stellt Zugriff auf die Eigenschaften der primären X‑Achse des Diagramms bereit.

 **Examples:** 

Zeigt, wie man ein Diagramm einfügt und das Aussehen seiner Achsen ändert.

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
[ChartAxis](../../com.aspose.words/chartaxis/) - The corresponding [ChartAxis](../../com.aspose.words/chartaxis/) value.
### getAxisY() {#getAxisY}
```
public ChartAxis getAxisY()
```


Stellt Zugriff auf die Eigenschaften der primären Y‑Achse des Diagramms bereit.

 **Examples:** 

Zeigt, wie man ein Diagramm einfügt und das Aussehen seiner Achsen ändert.

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
[ChartAxis](../../com.aspose.words/chartaxis/) - The corresponding [ChartAxis](../../com.aspose.words/chartaxis/) value.
### getAxisZ() {#getAxisZ}
```
public ChartAxis getAxisZ()
```


Stellt Zugriff auf die Eigenschaften der Z‑Achse des Diagramms bereit.

 **Examples:** 

Zeigt, wie man ein Diagramm einfügt und das Aussehen seiner Achsen ändert.

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
[ChartAxis](../../com.aspose.words/chartaxis/) - The corresponding [ChartAxis](../../com.aspose.words/chartaxis/) value.
### getDataTable() {#getDataTable}
```
public ChartDataTable getDataTable()
```


Stellt Zugriff auf Eigenschaften einer Datentabelle dieses Diagramms bereit. Die Datentabelle kann über die [ChartDataTable.getShow()](../../com.aspose.words/chartdatatable/\#getShow) / [ChartDataTable.setShow(boolean)](../../com.aspose.words/chartdatatable/\#setShow-boolean) Eigenschaft angezeigt werden.

 **Examples:** 

Zeigt, wie man die Datentabelle mit den Diagrammseriendaten anzeigt.

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
[ChartDataTable](../../com.aspose.words/chartdatatable/) - The corresponding [ChartDataTable](../../com.aspose.words/chartdatatable/) value.
### getFormat() {#getFormat}
```
public ChartFormat getFormat()
```


Stellt Zugriff auf Füll‑ und Linienformatierung des Diagramms bereit.

 **Examples:** 

Zeigt, wie die Diagrammformatierung verwendet wird.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete series generated by default.
 ChartSeriesCollection series = chart.getSeries();
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2" };
 series.add("Series 1", categories, new double[] { 1.0, 2.0 });
 series.add("Series 2", categories, new double[] { 3.0, 4.0 });

 // Format chart background.
 chart.getFormat().getFill().solid(Color.darkGray);

 // Hide axis tick labels.
 chart.getAxisX().getTickLabels().setPosition(AxisTickLabelPosition.NONE);
 chart.getAxisY().getTickLabels().setPosition(AxisTickLabelPosition.NONE);

 // Format chart title.
 chart.getTitle().getFormat().getFill().solid(Color.yellow);

 // Format axis title.
 chart.getAxisX().getTitle().setShow(true);
 chart.getAxisX().getTitle().getFormat().getFill().solid(Color.yellow);

 // Format legend.
 chart.getLegend().getFormat().getFill().solid(Color.yellow);

 doc.save(getArtifactsDir() + "Charts.ChartFormat.docx");
 
```

**Returns:**
[ChartFormat](../../com.aspose.words/chartformat/) - The corresponding [ChartFormat](../../com.aspose.words/chartformat/) value.
### getLegend() {#getLegend}
```
public ChartLegend getLegend()
```


Stellt Zugriff auf die Eigenschaften der Diagrammlegende bereit.

 **Examples:** 

Zeigt, wie man das Erscheinungsbild der Diagrammlegende bearbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // Move the chart's legend to the top right corner.
 ChartLegend legend = chart.getLegend();
 legend.setPosition(LegendPosition.TOP_RIGHT);

 // Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
 legend.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartLegend.docx");
 
```

**Returns:**
[ChartLegend](../../com.aspose.words/chartlegend/) - The corresponding [ChartLegend](../../com.aspose.words/chartlegend/) value.
### getSeries() {#getSeries}
```
public ChartSeriesCollection getSeries()
```


Stellt Zugriff auf die Serien‑Sammlung bereit.

 **Examples:** 

Zeigt, wie man einen geeigneten Diagrammserientyp für einen Diagrammtyp erstellt.

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
[ChartSeriesCollection](../../com.aspose.words/chartseriescollection/) - The corresponding [ChartSeriesCollection](../../com.aspose.words/chartseriescollection/) value.
### getSeriesGroups() {#getSeriesGroups}
```
public ChartSeriesGroupCollection getSeriesGroups()
```


Stellt Zugriff auf eine Seriengruppen‑Sammlung dieses Diagramms bereit.

 **Examples:** 

Zeigt, wie man Lückenbreite und Überlappung konfiguriert.

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
[ChartSeriesGroupCollection](../../com.aspose.words/chartseriesgroupcollection/) - The corresponding [ChartSeriesGroupCollection](../../com.aspose.words/chartseriesgroupcollection/) value.
### getShapeType() {#getShapeType}
```
public int getShapeType()
```




**Returns:**
int
### getSourceFullName() {#getSourceFullName}
```
public String getSourceFullName()
```


Ermittelt den Pfad und Namen einer xls/xlsx‑Datei, mit der dieses Diagramm verknüpft ist.

 **Examples:** 

Zeigt, wie man den vollständigen Namen des externen xls/xlsx‑Dokuments abruft/setzt, wenn das Diagramm verknüpft ist.

```

 Document doc = new Document(getMyDir() + "Shape with linked chart.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 String sourceFullName = shape.getChart().getSourceFullName();
 Assert.assertTrue(sourceFullName.contains("Examples\\Data\\Spreadsheet.xlsx"));
 
```

**Returns:**
java.lang.String – Der Pfad und Name einer xls/xlsx‑Datei, mit der dieses Diagramm verknüpft ist.
### getStyle() {#getStyle}
```
public int getStyle()
```


Ermittelt den Stil des Diagramms.

**Returns:**
int – Der Stil des Diagramms. Der zurückgegebene Wert ist einer der [ChartStyle](../../com.aspose.words/chartstyle/) Konstanten.
### getTitle() {#getTitle}
```
public ChartTitle getTitle()
```


Stellt Zugriff auf die Eigenschaften des Diagrammtitels bereit.

 **Examples:** 

Zeigt, wie man ein Diagramm einfügt und einen Titel festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a chart shape with a document builder and get its chart.
 Shape chartShape = builder.insertChart(ChartType.BAR, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Use the "Title" property to give our chart a title, which appears at the top center of the chart area.
 ChartTitle title = chart.getTitle();
 title.setText("My Chart");
 title.getFont().setSize(15.0);
 title.getFont().setColor(Color.BLUE);

 // Set the "Show" property to "true" to make the title visible.
 title.setShow(true);

 // Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
 title.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartTitle.docx");
 
```

**Returns:**
[ChartTitle](../../com.aspose.words/charttitle/) - The corresponding [ChartTitle](../../com.aspose.words/charttitle/) value.
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int |  |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String}
```
public void setSourceFullName(String value)
```


Ermittelt den Pfad und Namen einer xls/xlsx‑Datei, mit der dieses Diagramm verknüpft ist.

 **Examples:** 

Zeigt, wie man den vollständigen Namen des externen xls/xlsx‑Dokuments abruft/setzt, wenn das Diagramm verknüpft ist.

```

 Document doc = new Document(getMyDir() + "Shape with linked chart.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 String sourceFullName = shape.getChart().getSourceFullName();
 Assert.assertTrue(sourceFullName.contains("Examples\\Data\\Spreadsheet.xlsx"));
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Pfad und Name einer xls/xlsx‑Datei, mit der dieses Diagramm verknüpft ist. |

### setStyle(int value) {#setStyle-int}
```
public void setStyle(int value)
```


Legt den Stil des Diagramms fest.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der Stil des Diagramms. Der Wert muss einer der [ChartStyle](../../com.aspose.words/chartstyle/) Konstanten sein. |

