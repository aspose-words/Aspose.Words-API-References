---
title: "AxisBound"
linktitle: "AxisBound"
second_title: "Aspose.Words pour Java"
description: "Représente la limite minimale ou maximale des valeurs d’axe en Java."
type: docs
weight: 22
url: /fr/java/com.aspose.words/axisbound/
---

**Inheritance:**
java.lang.Object
```
public class AxisBound
```

Représente la borne minimale ou maximale des valeurs d'axe.

Pour en savoir plus, consultez l'article de documentation [ Working with Charts ][Working with Charts].

 **Remarks:** 

La limite peut être spécifiée comme une valeur numérique, une date/heure ou une valeur spéciale "auto".

Les instances de cette classe sont immuables.

 **Examples:** 

Montre comment insérer un graphique avec des valeurs de date/heure.

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


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Constructors

| Constructor | Description |
| --- | --- |
| [AxisBound()](#AxisBound) | Crée une nouvelle instance indiquant que la limite d’axe doit être déterminée automatiquement par une application de traitement de texte. |
| [AxisBound(double value)](#AxisBound-double) | Crée une limite d’axe représentée sous forme de nombre. |
| [AxisBound(Date datetime)](#AxisBound-java.util.Date) | Crée une limite d’axe représentée sous forme de valeur date/heure. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| [getValue()](#getValue) | Renvoie la valeur numérique de la limite d’axe. |
| [getValueAsDate()](#getValueAsDate) | Renvoie la valeur de la limite d'axe représentée sous forme de datetime. |
| [hashCode()](#hashCode) |  |
| [isAuto()](#isAuto) | Renvoie un indicateur indiquant que la limite d'axe doit être déterminée automatiquement. |
| [toString()](#toString) | Renvoie une chaîne conviviale qui affiche la valeur de cet objet. |
### AxisBound() {#AxisBound}
```
public AxisBound()
```


Crée une nouvelle instance indiquant que la limite d’axe doit être déterminée automatiquement par une application de traitement de texte.

 **Examples:** 

Montre comment définir des limites d'axe personnalisées.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a series with two decimal arrays. The first array contains the X-values,
 // and the second contains corresponding Y-values for points in the scatter chart.
 chart.getSeries().add("Series 1",
         new double[]{1.1, 5.4, 7.9, 3.5, 2.1, 9.7},
         new double[]{2.1, 0.3, 0.6, 3.3, 1.4, 1.9});

 // By default, default scaling is applied to the graph's X and Y-axes,
 // so that both their ranges are big enough to encompass every X and Y-value of every series.
 Assert.assertTrue(chart.getAxisX().getScaling().getMinimum().isAuto());

 // We can define our own axis bounds.
 // In this case, we will make both the X and Y-axis rulers show a range of 0 to 10.
 chart.getAxisX().getScaling().setMinimum(new AxisBound(0.0));
 chart.getAxisX().getScaling().setMaximum(new AxisBound(10.0));
 chart.getAxisY().getScaling().setMinimum(new AxisBound(0.0));
 chart.getAxisY().getScaling().setMaximum(new AxisBound(10.0));

 Assert.assertFalse(chart.getAxisX().getScaling().getMinimum().isAuto());
 Assert.assertFalse(chart.getAxisY().getScaling().getMinimum().isAuto());

 // Create a line chart with a series requiring a range of dates on the X-axis, and decimal values for the Y-axis.
 chartShape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 chart = chartShape.getChart();
 chart.getSeries().clear();

 Date[] dates = {DocumentHelper.createDate(1973, 5, 11),
         DocumentHelper.createDate(1981, 2, 4),
         DocumentHelper.createDate(1985, 9, 23),
         DocumentHelper.createDate(1989, 6, 28),
         DocumentHelper.createDate(1994, 12, 15)
 };

 chart.getSeries().add("Series 1", dates, new double[]{3.0, 4.7, 5.9, 7.1, 8.9});

 // We can set axis bounds in the form of dates as well, limiting the chart to a period.
 // Setting the range to 1980-1990 will omit the two of the series values
 // that are outside of the range from the graph.

 Date datetimeMin = DocumentHelper.createDate(1980, 1, 1);
 chart.getAxisX().getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(1980, 1, 1);
 chart.getAxisX().getScaling().setMaximum(new AxisBound(datetimeMax));

 doc.save(getArtifactsDir() + "Charts.AxisBound.docx");
 
```

### AxisBound(double value) {#AxisBound-double}
```
public AxisBound(double value)
```


Crée une limite d’axe représentée sous forme de nombre.

 **Examples:** 

Montre comment insérer un graphique avec des valeurs de date/heure.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double |  |

### AxisBound(Date datetime) {#AxisBound-java.util.Date}
```
public AxisBound(Date datetime)
```


Crée une limite d’axe représentée sous forme de valeur date/heure.

 **Examples:** 

Montre comment insérer un graphique avec des valeurs de date/heure.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| datetime | java.util.Date |  |

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Détermine si l'objet spécifié est égal en valeur à l'objet actuel.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getValue() {#getValue}
```
public double getValue()
```


Renvoie la valeur numérique de la limite d’axe.

 **Examples:** 

Montre comment définir des limites d'axe personnalisées.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a series with two decimal arrays. The first array contains the X-values,
 // and the second contains corresponding Y-values for points in the scatter chart.
 chart.getSeries().add("Series 1",
         new double[]{1.1, 5.4, 7.9, 3.5, 2.1, 9.7},
         new double[]{2.1, 0.3, 0.6, 3.3, 1.4, 1.9});

 // By default, default scaling is applied to the graph's X and Y-axes,
 // so that both their ranges are big enough to encompass every X and Y-value of every series.
 Assert.assertTrue(chart.getAxisX().getScaling().getMinimum().isAuto());

 // We can define our own axis bounds.
 // In this case, we will make both the X and Y-axis rulers show a range of 0 to 10.
 chart.getAxisX().getScaling().setMinimum(new AxisBound(0.0));
 chart.getAxisX().getScaling().setMaximum(new AxisBound(10.0));
 chart.getAxisY().getScaling().setMinimum(new AxisBound(0.0));
 chart.getAxisY().getScaling().setMaximum(new AxisBound(10.0));

 Assert.assertFalse(chart.getAxisX().getScaling().getMinimum().isAuto());
 Assert.assertFalse(chart.getAxisY().getScaling().getMinimum().isAuto());

 // Create a line chart with a series requiring a range of dates on the X-axis, and decimal values for the Y-axis.
 chartShape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 chart = chartShape.getChart();
 chart.getSeries().clear();

 Date[] dates = {DocumentHelper.createDate(1973, 5, 11),
         DocumentHelper.createDate(1981, 2, 4),
         DocumentHelper.createDate(1985, 9, 23),
         DocumentHelper.createDate(1989, 6, 28),
         DocumentHelper.createDate(1994, 12, 15)
 };

 chart.getSeries().add("Series 1", dates, new double[]{3.0, 4.7, 5.9, 7.1, 8.9});

 // We can set axis bounds in the form of dates as well, limiting the chart to a period.
 // Setting the range to 1980-1990 will omit the two of the series values
 // that are outside of the range from the graph.

 Date datetimeMin = DocumentHelper.createDate(1980, 1, 1);
 chart.getAxisX().getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(1980, 1, 1);
 chart.getAxisX().getScaling().setMaximum(new AxisBound(datetimeMax));

 doc.save(getArtifactsDir() + "Charts.AxisBound.docx");
 
```

**Returns:**
double - Valeur numérique de la limite d'axe.
### getValueAsDate() {#getValueAsDate}
```
public Date getValueAsDate()
```


Renvoie la valeur de la limite d'axe représentée sous forme de datetime.

 **Examples:** 

Montre comment définir des limites d'axe personnalisées.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a series with two decimal arrays. The first array contains the X-values,
 // and the second contains corresponding Y-values for points in the scatter chart.
 chart.getSeries().add("Series 1",
         new double[]{1.1, 5.4, 7.9, 3.5, 2.1, 9.7},
         new double[]{2.1, 0.3, 0.6, 3.3, 1.4, 1.9});

 // By default, default scaling is applied to the graph's X and Y-axes,
 // so that both their ranges are big enough to encompass every X and Y-value of every series.
 Assert.assertTrue(chart.getAxisX().getScaling().getMinimum().isAuto());

 // We can define our own axis bounds.
 // In this case, we will make both the X and Y-axis rulers show a range of 0 to 10.
 chart.getAxisX().getScaling().setMinimum(new AxisBound(0.0));
 chart.getAxisX().getScaling().setMaximum(new AxisBound(10.0));
 chart.getAxisY().getScaling().setMinimum(new AxisBound(0.0));
 chart.getAxisY().getScaling().setMaximum(new AxisBound(10.0));

 Assert.assertFalse(chart.getAxisX().getScaling().getMinimum().isAuto());
 Assert.assertFalse(chart.getAxisY().getScaling().getMinimum().isAuto());

 // Create a line chart with a series requiring a range of dates on the X-axis, and decimal values for the Y-axis.
 chartShape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 chart = chartShape.getChart();
 chart.getSeries().clear();

 Date[] dates = {DocumentHelper.createDate(1973, 5, 11),
         DocumentHelper.createDate(1981, 2, 4),
         DocumentHelper.createDate(1985, 9, 23),
         DocumentHelper.createDate(1989, 6, 28),
         DocumentHelper.createDate(1994, 12, 15)
 };

 chart.getSeries().add("Series 1", dates, new double[]{3.0, 4.7, 5.9, 7.1, 8.9});

 // We can set axis bounds in the form of dates as well, limiting the chart to a period.
 // Setting the range to 1980-1990 will omit the two of the series values
 // that are outside of the range from the graph.

 Date datetimeMin = DocumentHelper.createDate(1980, 1, 1);
 chart.getAxisX().getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(1980, 1, 1);
 chart.getAxisX().getScaling().setMaximum(new AxisBound(datetimeMax));

 doc.save(getArtifactsDir() + "Charts.AxisBound.docx");
 
```

**Returns:**
java.util.Date - Valeur de la limite d'axe représentée sous forme de datetime.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isAuto() {#isAuto}
```
public boolean isAuto()
```


Renvoie un indicateur indiquant que la limite d'axe doit être déterminée automatiquement.

 **Examples:** 

Montre comment définir des limites d'axe personnalisées.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a series with two decimal arrays. The first array contains the X-values,
 // and the second contains corresponding Y-values for points in the scatter chart.
 chart.getSeries().add("Series 1",
         new double[]{1.1, 5.4, 7.9, 3.5, 2.1, 9.7},
         new double[]{2.1, 0.3, 0.6, 3.3, 1.4, 1.9});

 // By default, default scaling is applied to the graph's X and Y-axes,
 // so that both their ranges are big enough to encompass every X and Y-value of every series.
 Assert.assertTrue(chart.getAxisX().getScaling().getMinimum().isAuto());

 // We can define our own axis bounds.
 // In this case, we will make both the X and Y-axis rulers show a range of 0 to 10.
 chart.getAxisX().getScaling().setMinimum(new AxisBound(0.0));
 chart.getAxisX().getScaling().setMaximum(new AxisBound(10.0));
 chart.getAxisY().getScaling().setMinimum(new AxisBound(0.0));
 chart.getAxisY().getScaling().setMaximum(new AxisBound(10.0));

 Assert.assertFalse(chart.getAxisX().getScaling().getMinimum().isAuto());
 Assert.assertFalse(chart.getAxisY().getScaling().getMinimum().isAuto());

 // Create a line chart with a series requiring a range of dates on the X-axis, and decimal values for the Y-axis.
 chartShape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 chart = chartShape.getChart();
 chart.getSeries().clear();

 Date[] dates = {DocumentHelper.createDate(1973, 5, 11),
         DocumentHelper.createDate(1981, 2, 4),
         DocumentHelper.createDate(1985, 9, 23),
         DocumentHelper.createDate(1989, 6, 28),
         DocumentHelper.createDate(1994, 12, 15)
 };

 chart.getSeries().add("Series 1", dates, new double[]{3.0, 4.7, 5.9, 7.1, 8.9});

 // We can set axis bounds in the form of dates as well, limiting the chart to a period.
 // Setting the range to 1980-1990 will omit the two of the series values
 // that are outside of the range from the graph.

 Date datetimeMin = DocumentHelper.createDate(1980, 1, 1);
 chart.getAxisX().getScaling().setMinimum(new AxisBound(datetimeMin));
 Date datetimeMax = DocumentHelper.createDate(1980, 1, 1);
 chart.getAxisX().getScaling().setMaximum(new AxisBound(datetimeMax));

 doc.save(getArtifactsDir() + "Charts.AxisBound.docx");
 
```

**Returns:**
boolean - Un indicateur indiquant que la limite d'axe doit être déterminée automatiquement.
### toString() {#toString}
```
public String toString()
```


Renvoie une chaîne conviviale qui affiche la valeur de cet objet.

**Returns:**
java.lang.String
