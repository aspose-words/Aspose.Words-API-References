---
title: "AxisGroup"
linktitle: "AxisGroup"
second_title: "Aspose.Words per Java"
description: "Rappresenta un tipo di gruppo di assi di un grafico in Java."
type: docs
weight: 27
url: /it/java/com.aspose.words/axisgroup/
---

**Inheritance:**
java.lang.Object
```
public class AxisGroup
```

Rappresenta un tipo di gruppo di assi del grafico.

 **Examples:** 

Mostra come lavorare con l'asse secondario del grafico.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [PRIMARY](#PRIMARY) | Specifica il gruppo di assi primario. |
| [SECONDARY](#SECONDARY) | Specifica il gruppo di assi secondario. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String axisGroupName)](#fromName-java.lang.String) |  |
| [getName(int axisGroup)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisGroup)](#toString-int) |  |
### PRIMARY {#PRIMARY}
```
public static int PRIMARY
```


Specifica il gruppo di assi primario.

### SECONDARY {#SECONDARY}
```
public static int SECONDARY
```


Specifica il gruppo di assi secondario.

### length {#length}
```
public static int length
```


### fromName(String axisGroupName) {#fromName-java.lang.String}
```
public static int fromName(String axisGroupName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| axisGroupName | java.lang.String |  |

**Returns:**
int
### getName(int axisGroup) {#getName-int}
```
public static String getName(int axisGroup)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| axisGroup | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int axisGroup) {#toString-int}
```
public static String toString(int axisGroup)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| axisGroup | int |  |

**Returns:**
java.lang.String
