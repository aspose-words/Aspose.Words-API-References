---
title: "AxisScaling"
linktitle: "AxisScaling"
second_title: "Aspose.Words pour Java"
description: "Représente les options de mise à l'échelle de l'axe en Java."
type: docs
weight: 29
url: /fr/java/com.aspose.words/axisscaling/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class AxisScaling implements Cloneable
```

Représente les options de mise à l'échelle de l'axe.

Pour en savoir plus, consultez l'article de documentation [ Working with Charts ][Working with Charts].

 **Examples:** 

Montre comment appliquer un échelonnage logarithmique à un axe de graphique.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a series with X/Y coordinates for five points.
 chart.getSeries().add("Series 1",
         new double[]{1.0, 2.0, 3.0, 4.0, 5.0},
         new double[]{1.0, 20.0, 400.0, 8000.0, 160000.0});

 // The scaling of the X-axis is linear by default,
 // displaying evenly incrementing values that cover our X-value range (0, 1, 2, 3...).
 // A linear axis is not ideal for our Y-values
 // since the points with the smaller Y-values will be harder to read.
 // A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
 // will spread the plotted points, allowing us to read their values on the chart more easily.
 chart.getAxisY().getScaling().setType(AxisScaleType.LOGARITHMIC);
 chart.getAxisY().getScaling().setLogBase(20.0);

 doc.save(getArtifactsDir() + "Charts.AxisScaling.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Méthodes

| Méthode | Description |
| --- | --- |
| [getLogBase()](#getLogBase) | Obtient la base logarithmique d'un axe logarithmique. |
| [getMaximum()](#getMaximum) | Obtient la valeur maximale de l'axe. |
| [getMinimum()](#getMinimum) | Obtient la valeur minimale de l'axe. |
| [getType()](#getType) | Obtient le type de mise à l'échelle de l'axe. |
| [setLogBase(double value)](#setLogBase-double) | Définit la base logarithmique d'un axe logarithmique. |
| [setMaximum(AxisBound value)](#setMaximum-com.aspose.words.AxisBound) | Définit la valeur maximale de l'axe. |
| [setMinimum(AxisBound value)](#setMinimum-com.aspose.words.AxisBound) | Définit la valeur minimale de l'axe. |
| [setType(int value)](#setType-int) | Définit le type de mise à l'échelle de l'axe. |
### getLogBase() {#getLogBase}
```
public double getLogBase()
```


Obtient la base logarithmique d'un axe logarithmique.

 **Remarks:** 

La propriété n'est pas prise en charge par les nouveaux graphiques de MS Office 2016.

La plage valide d'une valeur à virgule flottante est supérieure ou égale à 2 et inférieure ou égale à 1000. La propriété n'a d'effet que si [getType()](../../com.aspose.words/axisscaling/\#getType) / [setType(int)](../../com.aspose.words/axisscaling/\#setType-int) est définie sur [AxisScaleType.LOGARITHMIC](../../com.aspose.words/axisscaletype/\#LOGARITHMIC).

Définir cette propriété affecte la propriété [getType()](../../com.aspose.words/axisscaling/\#getType) / [setType(int)](../../com.aspose.words/axisscaling/\#setType-int) à [AxisScaleType.LOGARITHMIC](../../com.aspose.words/axisscaletype/\#LOGARITHMIC).

 **Examples:** 

Montre comment appliquer un échelonnage logarithmique à un axe de graphique.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a series with X/Y coordinates for five points.
 chart.getSeries().add("Series 1",
         new double[]{1.0, 2.0, 3.0, 4.0, 5.0},
         new double[]{1.0, 20.0, 400.0, 8000.0, 160000.0});

 // The scaling of the X-axis is linear by default,
 // displaying evenly incrementing values that cover our X-value range (0, 1, 2, 3...).
 // A linear axis is not ideal for our Y-values
 // since the points with the smaller Y-values will be harder to read.
 // A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
 // will spread the plotted points, allowing us to read their values on the chart more easily.
 chart.getAxisY().getScaling().setType(AxisScaleType.LOGARITHMIC);
 chart.getAxisY().getScaling().setLogBase(20.0);

 doc.save(getArtifactsDir() + "Charts.AxisScaling.docx");
 
```

**Returns:**
double - La base logarithmique d'un axe logarithmique.
### getMaximum() {#getMaximum}
```
public AxisBound getMaximum()
```


Obtient la valeur maximale de l'axe.

 **Remarks:** 

La valeur par défaut est "auto".

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

**Returns:**
[AxisBound](../../com.aspose.words/axisbound/) - The maximum value of the axis.
### getMinimum() {#getMinimum}
```
public AxisBound getMinimum()
```


Obtient la valeur minimale de l'axe.

 **Remarks:** 

La valeur par défaut est "auto".

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

**Returns:**
[AxisBound](../../com.aspose.words/axisbound/) - Minimum value of the axis.
### getType() {#getType}
```
public int getType()
```


Obtient le type de mise à l'échelle de l'axe.

 **Remarks:** 

La valeur [AxisScaleType.LINEAR](../../com.aspose.words/axisscaletype/\#LINEAR) est la seule autorisée dans les nouveaux graphiques de MS Office 2016.

 **Examples:** 

Montre comment appliquer un échelonnage logarithmique à un axe de graphique.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a series with X/Y coordinates for five points.
 chart.getSeries().add("Series 1",
         new double[]{1.0, 2.0, 3.0, 4.0, 5.0},
         new double[]{1.0, 20.0, 400.0, 8000.0, 160000.0});

 // The scaling of the X-axis is linear by default,
 // displaying evenly incrementing values that cover our X-value range (0, 1, 2, 3...).
 // A linear axis is not ideal for our Y-values
 // since the points with the smaller Y-values will be harder to read.
 // A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
 // will spread the plotted points, allowing us to read their values on the chart more easily.
 chart.getAxisY().getScaling().setType(AxisScaleType.LOGARITHMIC);
 chart.getAxisY().getScaling().setLogBase(20.0);

 doc.save(getArtifactsDir() + "Charts.AxisScaling.docx");
 
```

**Returns:**
int - Type de mise à l'échelle de l'axe. La valeur retournée est l'une des constantes [AxisScaleType](../../com.aspose.words/axisscaletype/).
### setLogBase(double value) {#setLogBase-double}
```
public void setLogBase(double value)
```


Définit la base logarithmique d'un axe logarithmique.

 **Remarks:** 

La propriété n'est pas prise en charge par les nouveaux graphiques de MS Office 2016.

La plage valide d'une valeur à virgule flottante est supérieure ou égale à 2 et inférieure ou égale à 1000. La propriété n'a d'effet que si [getType()](../../com.aspose.words/axisscaling/\#getType) / [setType(int)](../../com.aspose.words/axisscaling/\#setType-int) est définie sur [AxisScaleType.LOGARITHMIC](../../com.aspose.words/axisscaletype/\#LOGARITHMIC).

Définir cette propriété affecte la propriété [getType()](../../com.aspose.words/axisscaling/\#getType) / [setType(int)](../../com.aspose.words/axisscaling/\#setType-int) à [AxisScaleType.LOGARITHMIC](../../com.aspose.words/axisscaletype/\#LOGARITHMIC).

 **Examples:** 

Montre comment appliquer un échelonnage logarithmique à un axe de graphique.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a series with X/Y coordinates for five points.
 chart.getSeries().add("Series 1",
         new double[]{1.0, 2.0, 3.0, 4.0, 5.0},
         new double[]{1.0, 20.0, 400.0, 8000.0, 160000.0});

 // The scaling of the X-axis is linear by default,
 // displaying evenly incrementing values that cover our X-value range (0, 1, 2, 3...).
 // A linear axis is not ideal for our Y-values
 // since the points with the smaller Y-values will be harder to read.
 // A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
 // will spread the plotted points, allowing us to read their values on the chart more easily.
 chart.getAxisY().getScaling().setType(AxisScaleType.LOGARITHMIC);
 chart.getAxisY().getScaling().setLogBase(20.0);

 doc.save(getArtifactsDir() + "Charts.AxisScaling.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | double | La base logarithmique d'un axe logarithmique. |

### setMaximum(AxisBound value) {#setMaximum-com.aspose.words.AxisBound}
```
public void setMaximum(AxisBound value)
```


Définit la valeur maximale de l'axe.

 **Remarks:** 

La valeur par défaut est "auto".

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
| value | [AxisBound](../../com.aspose.words/axisbound/) | La valeur maximale de l'axe. |

### setMinimum(AxisBound value) {#setMinimum-com.aspose.words.AxisBound}
```
public void setMinimum(AxisBound value)
```


Définit la valeur minimale de l'axe.

 **Remarks:** 

La valeur par défaut est "auto".

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
| value | [AxisBound](../../com.aspose.words/axisbound/) | Valeur minimale de l'axe. |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


Définit le type de mise à l'échelle de l'axe.

 **Remarks:** 

La valeur [AxisScaleType.LINEAR](../../com.aspose.words/axisscaletype/\#LINEAR) est la seule autorisée dans les nouveaux graphiques de MS Office 2016.

 **Examples:** 

Montre comment appliquer un échelonnage logarithmique à un axe de graphique.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a series with X/Y coordinates for five points.
 chart.getSeries().add("Series 1",
         new double[]{1.0, 2.0, 3.0, 4.0, 5.0},
         new double[]{1.0, 20.0, 400.0, 8000.0, 160000.0});

 // The scaling of the X-axis is linear by default,
 // displaying evenly incrementing values that cover our X-value range (0, 1, 2, 3...).
 // A linear axis is not ideal for our Y-values
 // since the points with the smaller Y-values will be harder to read.
 // A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
 // will spread the plotted points, allowing us to read their values on the chart more easily.
 chart.getAxisY().getScaling().setType(AxisScaleType.LOGARITHMIC);
 chart.getAxisY().getScaling().setLogBase(20.0);

 doc.save(getArtifactsDir() + "Charts.AxisScaling.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Type d'échelle de l'axe. La valeur doit être l'une des constantes [AxisScaleType](../../com.aspose.words/axisscaletype/). |

