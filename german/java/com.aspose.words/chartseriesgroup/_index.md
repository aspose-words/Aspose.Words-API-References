---
title: "ChartSeriesGroup"
linktitle: "ChartSeriesGroup"
second_title: "Aspose.Words für Java"
description: "Stellt die Eigenschaften einer Diagrammseriengruppe dar, die die Eigenschaften von Diagrammserien desselben Typs sind, die mit denselben Achsen in Java verknüpft sind."
type: docs
weight: 87
url: /de/java/com.aspose.words/chartseriesgroup/
---

**Inheritance:**
java.lang.Object
```
public class ChartSeriesGroup
```

Stellt die Eigenschaften einer Diagrammseriengruppe dar, d.h. die Eigenschaften von Diagrammserien desselben Typs, die den gleichen Achsen zugeordnet sind.

 **Remarks:** 

Kombidiagramme enthalten mehrere Diagrammseriengruppen, wobei für jeden Serientyp eine separate Gruppe besteht.

Außerdem können Sie eine Diagrammseriengruppe erstellen, um sekundäre Achsen einer oder mehreren Diagrammserien zuzuweisen.

Weitere Informationen finden Sie im Dokumentationsartikel zu [ Working with Charts ][Working with Charts].

 **Examples:** 

Zeigt, wie man mit der sekundären Achse eines Diagramms arbeitet.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getAxisGroup()](#getAxisGroup) | Gibt die Achsengruppe zurück, zu der diese Seriengruppe gehört. |
| [getAxisX()](#getAxisX) | Bietet Zugriff auf die Eigenschaften der X‑Achse dieser Seriengruppe. |
| [getAxisY()](#getAxisY) | Bietet Zugriff auf die Eigenschaften der Y‑Achse dieser Seriengruppe. |
| [getBubbleScale()](#getBubbleScale) | Gibt die Größe der Blasen als Prozentsatz ihrer Standardgröße zurück. |
| [getDoughnutHoleSize()](#getDoughnutHoleSize) | Gibt die Lochgröße des übergeordneten Donut‑Diagramms als Prozentsatz zurück. |
| [getFirstSliceAngle()](#getFirstSliceAngle) | Gibt den Winkel in Grad des ersten Stücks des übergeordneten Kreisdiagramms zurück. |
| [getGapWidth()](#getGapWidth) | Gibt den Prozentsatz der Lückenbreite zwischen Diagrammelementen zurück. |
| [getOverlap()](#getOverlap) | Gibt den Prozentsatz an, wie stark die Serienbalken oder -spalten überlappen. |
| [getSecondSectionSize()](#getSecondSectionSize) | Gibt die Größe des sekundären Abschnitts des Kreisdiagramms als Prozentsatz zurück. |
| [getSeries()](#getSeries) | Gibt eine Sammlung von Serien zurück, die zu dieser Seriengruppe gehören. |
| [getSeriesType()](#getSeriesType) | Gibt den Typ der in dieser Gruppe enthaltenen Diagrammserien zurück. |
| [setAxisGroup(int value)](#setAxisGroup-int) | Legt die Achsengruppe fest, zu der diese Seriengruppe gehört. |
| [setBubbleScale(int value)](#setBubbleScale-int) | Legt die Größe der Blasen als Prozentsatz ihrer Standardgröße fest. |
| [setDoughnutHoleSize(int value)](#setDoughnutHoleSize-int) | Legt die Lochgröße des übergeordneten Donut‑Diagramms als Prozentsatz fest. |
| [setFirstSliceAngle(int value)](#setFirstSliceAngle-int) | Legt den Winkel in Grad des ersten Stücks des übergeordneten Kreisdiagramms fest. |
| [setGapWidth(int value)](#setGapWidth-int) | Legt den Prozentsatz der Lückenbreite zwischen Diagrammelementen fest. |
| [setOverlap(int value)](#setOverlap-int) | Legt den Prozentsatz fest, wie stark die Serienbalken oder -spalten überlappen. |
| [setSecondSectionSize(int value)](#setSecondSectionSize-int) | Legt die Größe des sekundären Abschnitts des Kreisdiagramms als Prozentsatz fest. |
### getAxisGroup() {#getAxisGroup}
```
public int getAxisGroup()
```


Gibt die Achsengruppe zurück, zu der diese Seriengruppe gehört.

 **Examples:** 

Zeigt, wie man mit der sekundären Achse eines Diagramms arbeitet.

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
int - Die Achsengruppe, zu der diese Seriengruppe gehört. Der zurückgegebene Wert ist einer der [AxisGroup](../../com.aspose.words/axisgroup/) Konstanten.
### getAxisX() {#getAxisX}
```
public ChartAxis getAxisX()
```


Bietet Zugriff auf die Eigenschaften der X‑Achse dieser Seriengruppe.

 **Examples:** 

Zeigt, wie man mit der sekundären Achse eines Diagramms arbeitet.

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


Bietet Zugriff auf die Eigenschaften der Y‑Achse dieser Seriengruppe.

 **Examples:** 

Zeigt, wie man mit der sekundären Achse eines Diagramms arbeitet.

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


Gibt die Größe der Blasen als Prozentsatz ihrer Standardgröße zurück.

 **Remarks:** 

Gilt nur für Seriengruppen des Typs [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE) und [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D) Typen.

Der zulässige Wertebereich liegt zwischen 0 und 300, inklusiv. Der Standardwert ist 100.

 **Examples:** 

Zeigt, wie die Größe der Blasen festgelegt wird.

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
int - Die Größe der Blasen als Prozentsatz ihrer Standardgröße.
### getDoughnutHoleSize() {#getDoughnutHoleSize}
```
public int getDoughnutHoleSize()
```


Gibt die Lochgröße des übergeordneten Donut‑Diagramms als Prozentsatz zurück.

 **Remarks:** 

Gilt nur für Seriengruppen des Typs [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT).

Der zulässige Wertebereich liegt zwischen 0 und 90, inklusiv. Der Standardwert ist 75.

 **Examples:** 

Zeigt, wie ein Doughnut-Diagramm erstellt und formatiert wird.

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
int - Die Lochgröße des übergeordneten Doughnut-Diagramms als Prozentsatz.
### getFirstSliceAngle() {#getFirstSliceAngle}
```
public int getFirstSliceAngle()
```


Gibt den Winkel in Grad des ersten Stücks des übergeordneten Kreisdiagramms zurück.

 **Remarks:** 

Gilt für Seriengruppen der Typen [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D) und [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT).

Der zulässige Wertebereich liegt zwischen 0 und 360, inklusiv. Der Standardwert ist 0.

 **Examples:** 

Zeigt, wie ein Doughnut-Diagramm erstellt und formatiert wird.

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
int - Der Winkel, in Grad, des ersten Stücks des übergeordneten Kreisdiagramms.
### getGapWidth() {#getGapWidth}
```
public int getGapWidth()
```


Gibt den Prozentsatz der Lückenbreite zwischen Diagrammelementen zurück.

 **Remarks:** 

Gilt nur für Seriengruppen der Typen Balken, Säule, Kuchen‑aus‑Balken, Kuchen‑aus‑Kuchen, Histogramm, Box‑&‑Whisker, Wasserfall und Trichter.

Der zulässige Wertebereich liegt zwischen 0 und 500, inklusiv. Für balken‑/säulenbasierte Seriengruppen stellt die Eigenschaft den Abstand zwischen Balkenclustern als Prozentsatz ihrer Breite dar. Für Kuchen‑aus‑Kuchen‑ und Balken‑aus‑Kuchen‑Diagramme ist dies der Abstand zwischen dem primären und dem sekundären Abschnitt des Diagramms.

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
int - Der Prozentsatz der Lückenbreite zwischen Diagrammelementen.
### getOverlap() {#getOverlap}
```
public int getOverlap()
```


Gibt den Prozentsatz an, wie stark die Serienbalken oder -spalten überlappen.

 **Remarks:** 

Gilt für Seriengruppen aller Balken‑ und Säulentypen.

Der zulässige Wertebereich liegt zwischen -100 und 100, inklusiv. Ein Wert von 0 bedeutet, dass kein Abstand zwischen Balken/Säulen besteht. Bei einem Wert von -100 ist der Abstand zwischen Balken/Säulen gleich ihrer Breite. Ein Wert von 100 bedeutet, dass sich die Balken/Säulen vollständig überlappen.

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
int - Der Prozentsatz, um den sich die Serienbalken oder -säulen überlappen.
### getSecondSectionSize() {#getSecondSectionSize}
```
public int getSecondSectionSize()
```


Gibt die Größe des sekundären Abschnitts des Kreisdiagramms als Prozentsatz zurück.

 **Remarks:** 

Gilt für Seriengruppen der Typen [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE) und [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR) Typen.

Der zulässige Wertebereich liegt zwischen 5 und 200, inklusiv. Der Standardwert ist 75.

 **Examples:** 

Zeigt, wie ein Pie‑of‑Pie-Diagramm erstellt und formatiert wird.

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
int - Die Größe des sekundären Abschnitts des Kreisdiagramms als Prozentsatz.
### getSeries() {#getSeries}
```
public ChartSeriesCollection getSeries()
```


Gibt eine Sammlung von Serien zurück, die zu dieser Seriengruppe gehören.

 **Examples:** 

Zeigt, wie man mit der sekundären Achse eines Diagramms arbeitet.

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


Gibt den Typ der in dieser Gruppe enthaltenen Diagrammserien zurück.

 **Examples:** 

Zeigt, wie man mit der sekundären Achse eines Diagramms arbeitet.

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
int - Der Typ der in dieser Gruppe enthaltenen Diagrammserien. Der zurückgegebene Wert ist einer der [ChartSeriesType](../../com.aspose.words/chartseriestype/) Konstanten.
### setAxisGroup(int value) {#setAxisGroup-int}
```
public void setAxisGroup(int value)
```


Legt die Achsengruppe fest, zu der diese Seriengruppe gehört.

 **Examples:** 

Zeigt, wie man mit der sekundären Achse eines Diagramms arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Die Achsengruppe, zu der diese Seriengruppe gehört. Der Wert muss einer der [AxisGroup](../../com.aspose.words/axisgroup/) Konstanten sein. |

### setBubbleScale(int value) {#setBubbleScale-int}
```
public void setBubbleScale(int value)
```


Legt die Größe der Blasen als Prozentsatz ihrer Standardgröße fest.

 **Remarks:** 

Gilt nur für Seriengruppen des Typs [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE) und [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D) Typen.

Der zulässige Wertebereich liegt zwischen 0 und 300, inklusiv. Der Standardwert ist 100.

 **Examples:** 

Zeigt, wie die Größe der Blasen festgelegt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Die Größe der Blasen als Prozentsatz ihrer Standardgröße. |

### setDoughnutHoleSize(int value) {#setDoughnutHoleSize-int}
```
public void setDoughnutHoleSize(int value)
```


Legt die Lochgröße des übergeordneten Donut‑Diagramms als Prozentsatz fest.

 **Remarks:** 

Gilt nur für Seriengruppen des Typs [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT).

Der zulässige Wertebereich liegt zwischen 0 und 90, inklusiv. Der Standardwert ist 75.

 **Examples:** 

Zeigt, wie ein Doughnut-Diagramm erstellt und formatiert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Die Lochgröße des übergeordneten Donut-Diagramms als Prozentsatz. |

### setFirstSliceAngle(int value) {#setFirstSliceAngle-int}
```
public void setFirstSliceAngle(int value)
```


Legt den Winkel in Grad des ersten Stücks des übergeordneten Kreisdiagramms fest.

 **Remarks:** 

Gilt für Seriengruppen der Typen [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D) und [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT).

Der zulässige Wertebereich liegt zwischen 0 und 360, inklusiv. Der Standardwert ist 0.

 **Examples:** 

Zeigt, wie ein Doughnut-Diagramm erstellt und formatiert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der Winkel, in Grad, des ersten Stücks des übergeordneten Kreisdiagramms. |

### setGapWidth(int value) {#setGapWidth-int}
```
public void setGapWidth(int value)
```


Legt den Prozentsatz der Lückenbreite zwischen Diagrammelementen fest.

 **Remarks:** 

Gilt nur für Seriengruppen der Typen Balken, Säule, Kuchen‑aus‑Balken, Kuchen‑aus‑Kuchen, Histogramm, Box‑&‑Whisker, Wasserfall und Trichter.

Der zulässige Wertebereich liegt zwischen 0 und 500, inklusiv. Für balken‑/säulenbasierte Seriengruppen stellt die Eigenschaft den Abstand zwischen Balkenclustern als Prozentsatz ihrer Breite dar. Für Kuchen‑aus‑Kuchen‑ und Balken‑aus‑Kuchen‑Diagramme ist dies der Abstand zwischen dem primären und dem sekundären Abschnitt des Diagramms.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der Prozentsatz der Lückenbreite zwischen Diagrammelementen. |

### setOverlap(int value) {#setOverlap-int}
```
public void setOverlap(int value)
```


Legt den Prozentsatz fest, wie stark die Serienbalken oder -spalten überlappen.

 **Remarks:** 

Gilt für Seriengruppen aller Balken‑ und Säulentypen.

Der zulässige Wertebereich liegt zwischen -100 und 100, inklusiv. Ein Wert von 0 bedeutet, dass kein Abstand zwischen Balken/Säulen besteht. Bei einem Wert von -100 ist der Abstand zwischen Balken/Säulen gleich ihrer Breite. Ein Wert von 100 bedeutet, dass sich die Balken/Säulen vollständig überlappen.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der Prozentsatz, wie stark die Balken oder Spalten der Serie überlappen. |

### setSecondSectionSize(int value) {#setSecondSectionSize-int}
```
public void setSecondSectionSize(int value)
```


Legt die Größe des sekundären Abschnitts des Kreisdiagramms als Prozentsatz fest.

 **Remarks:** 

Gilt für Seriengruppen der Typen [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE) und [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR) Typen.

Der zulässige Wertebereich liegt zwischen 5 und 200, inklusiv. Der Standardwert ist 75.

 **Examples:** 

Zeigt, wie ein Pie‑of‑Pie-Diagramm erstellt und formatiert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Die Größe des sekundären Abschnitts des Kreisdiagramms als Prozentsatz. |

