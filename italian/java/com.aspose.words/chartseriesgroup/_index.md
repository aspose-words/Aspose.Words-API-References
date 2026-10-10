---
title: "ChartSeriesGroup"
linktitle: "ChartSeriesGroup"
second_title: "Aspose.Words per Java"
description: "Rappresenta le proprietà di un gruppo di serie di grafico, ovvero le proprietà delle serie di grafico dello stesso tipo associate agli stessi assi in Java."
type: docs
weight: 87
url: /it/java/com.aspose.words/chartseriesgroup/
---

**Inheritance:**
java.lang.Object
```
public class ChartSeriesGroup
```

Rappresenta le proprietà di un gruppo di serie del grafico, cioè le proprietà delle serie del grafico dello stesso tipo associate agli stessi assi.

 **Remarks:** 

I grafici combinati contengono più gruppi di serie di grafico, con un gruppo separato per ogni tipo di serie.

Inoltre, è possibile creare un gruppo di serie di grafico per assegnare assi secondari a una o più serie di grafico.

Per saperne di più, visita l'articolo di documentazione [ Working with Charts ][Working with Charts].

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


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getAxisGroup()](#getAxisGroup) | Ottiene il gruppo di assi a cui appartiene questo gruppo di serie. |
| [getAxisX()](#getAxisX) | Fornisce l'accesso alle proprietà dell'asse X di questo gruppo di serie. |
| [getAxisY()](#getAxisY) | Fornisce l'accesso alle proprietà dell'asse Y di questo gruppo di serie. |
| [getBubbleScale()](#getBubbleScale) | Ottiene la dimensione delle bolle come percentuale della loro dimensione predefinita. |
| [getDoughnutHoleSize()](#getDoughnutHoleSize) | Ottiene la dimensione del foro del grafico a ciambella principale come percentuale. |
| [getFirstSliceAngle()](#getFirstSliceAngle) | Ottiene l'angolo, in gradi, della prima fetta del grafico a torta principale. |
| [getGapWidth()](#getGapWidth) | Ottiene la percentuale della larghezza dello spazio tra gli elementi del grafico. |
| [getOverlap()](#getOverlap) | Ottiene la percentuale di quanto le barre o le colonne della serie si sovrappongono. |
| [getSecondSectionSize()](#getSecondSectionSize) | Ottiene la dimensione della sezione secondaria del grafico a torta come percentuale. |
| [getSeries()](#getSeries) | Ottiene una raccolta di serie che appartengono a questo gruppo di serie. |
| [getSeriesType()](#getSeriesType) | Ottiene il tipo di serie di grafico inclusa in questo gruppo. |
| [setAxisGroup(int value)](#setAxisGroup-int) | Imposta il gruppo di assi a cui appartiene questo gruppo di serie. |
| [setBubbleScale(int value)](#setBubbleScale-int) | Imposta la dimensione delle bolle come percentuale della loro dimensione predefinita. |
| [setDoughnutHoleSize(int value)](#setDoughnutHoleSize-int) | Imposta la dimensione del foro del grafico a ciambella principale come percentuale. |
| [setFirstSliceAngle(int value)](#setFirstSliceAngle-int) | Imposta l'angolo, in gradi, della prima fetta del grafico a torta principale. |
| [setGapWidth(int value)](#setGapWidth-int) | Imposta la percentuale della larghezza dello spazio tra gli elementi del grafico. |
| [setOverlap(int value)](#setOverlap-int) | Imposta la percentuale di quanto le barre o le colonne della serie si sovrappongono. |
| [setSecondSectionSize(int value)](#setSecondSectionSize-int) | Imposta la dimensione della sezione secondaria del grafico a torta come percentuale. |
### getAxisGroup() {#getAxisGroup}
```
public int getAxisGroup()
```


Ottiene il gruppo di assi a cui appartiene questo gruppo di serie.

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

**Returns:**
int - Il gruppo di assi a cui appartiene questo gruppo di serie. Il valore restituito è una delle costanti [AxisGroup](../../com.aspose.words/axisgroup/) .
### getAxisX() {#getAxisX}
```
public ChartAxis getAxisX()
```


Fornisce l'accesso alle proprietà dell'asse X di questo gruppo di serie.

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

**Returns:**
[ChartAxis](../../com.aspose.words/chartaxis/) - The corresponding [ChartAxis](../../com.aspose.words/chartaxis/) value.
### getAxisY() {#getAxisY}
```
public ChartAxis getAxisY()
```


Fornisce l'accesso alle proprietà dell'asse Y di questo gruppo di serie.

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

**Returns:**
[ChartAxis](../../com.aspose.words/chartaxis/) - The corresponding [ChartAxis](../../com.aspose.words/chartaxis/) value.
### getBubbleScale() {#getBubbleScale}
```
public int getBubbleScale()
```


Ottiene la dimensione delle bolle come percentuale della loro dimensione predefinita.

 **Remarks:** 

Si applica solo ai gruppi di serie del tipo [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE) e [ChartSeriesType.BUBBLE_3_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D).

L'intervallo di valori accettabili è da 0 a 300 inclusi. Il valore predefinito è 100.

 **Examples:** 

Mostra come impostare la dimensione delle bolle.

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
int - La dimensione delle bolle come percentuale della loro dimensione predefinita.
### getDoughnutHoleSize() {#getDoughnutHoleSize}
```
public int getDoughnutHoleSize()
```


Ottiene la dimensione del foro del grafico a ciambella principale come percentuale.

 **Remarks:** 

Si applica solo ai gruppi di serie del tipo [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT).

L'intervallo di valori accettabili è da 0 a 90 inclusi. Il valore predefinito è 75.

 **Examples:** 

Mostra come creare e formattare un grafico a ciambella.

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
int - La dimensione del foro del grafico a ciambella principale in percentuale.
### getFirstSliceAngle() {#getFirstSliceAngle}
```
public int getFirstSliceAngle()
```


Ottiene l'angolo, in gradi, della prima fetta del grafico a torta principale.

 **Remarks:** 

Si applica ai gruppi di serie dei tipi [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D) e [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT).

L'intervallo di valori accettabili è da 0 a 360 inclusi. Il valore predefinito è 0.

 **Examples:** 

Mostra come creare e formattare un grafico a ciambella.

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
int - L'angolo, in gradi, della prima fetta del grafico a torta principale.
### getGapWidth() {#getGapWidth}
```
public int getGapWidth()
```


Ottiene la percentuale della larghezza dello spazio tra gli elementi del grafico.

 **Remarks:** 

Si applica solo ai gruppi di serie dei tipi barra, colonna, pie-of-bar, pie-of-pie, histogram, box&whisker, waterfall e funnel.

L'intervallo di valori accettabili è da 0 a 500 inclusi. Per i gruppi di serie basati su barra/colonna, la proprietà rappresenta lo spazio tra i raggruppamenti di barre come percentuale della loro larghezza. Per i grafici pie-of-pie e bar-of-pie, questo è lo spazio tra le sezioni primaria e secondaria del grafico.

 **Examples:** 

Mostra come configurare la larghezza dello spazio e la sovrapposizione.

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
int - La percentuale di larghezza dello spazio tra gli elementi del grafico.
### getOverlap() {#getOverlap}
```
public int getOverlap()
```


Ottiene la percentuale di quanto le barre o le colonne della serie si sovrappongono.

 **Remarks:** 

Si applica ai gruppi di serie di tutti i tipi barra e colonna.

L'intervallo di valori accettabili è da -100 a 100 inclusi. Un valore di 0 indica che non c'è spazio tra le barre/colonne. Se il valore è -100, la distanza tra le barre/colonne è pari alla loro larghezza. Un valore di 100 significa che le barre/colonne si sovrappongono completamente.

 **Examples:** 

Mostra come configurare la larghezza dello spazio e la sovrapposizione.

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
int - La percentuale di sovrapposizione delle barre o colonne della serie.
### getSecondSectionSize() {#getSecondSectionSize}
```
public int getSecondSectionSize()
```


Ottiene la dimensione della sezione secondaria del grafico a torta come percentuale.

 **Remarks:** 

Si applica ai gruppi di serie dei tipi [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE) e [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR).

L'intervallo di valori accettabili è da 5 a 200 inclusi. Il valore predefinito è 75.

 **Examples:** 

Mostra come creare e formattare un grafico torta su torta.

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
int - La dimensione della sezione secondaria del grafico a torta in percentuale.
### getSeries() {#getSeries}
```
public ChartSeriesCollection getSeries()
```


Ottiene una raccolta di serie che appartengono a questo gruppo di serie.

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

**Returns:**
[ChartSeriesCollection](../../com.aspose.words/chartseriescollection/) - A collection of series that belong to this series group.
### getSeriesType() {#getSeriesType}
```
public int getSeriesType()
```


Ottiene il tipo di serie di grafico inclusa in questo gruppo.

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

**Returns:**
int - Il tipo di serie di grafico incluso in questo gruppo. Il valore restituito è una delle costanti [ChartSeriesType](../../com.aspose.words/chartseriestype/).
### setAxisGroup(int value) {#setAxisGroup-int}
```
public void setAxisGroup(int value)
```


Imposta il gruppo di assi a cui appartiene questo gruppo di serie.

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

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il gruppo di assi a cui appartiene questo gruppo di serie. Il valore deve essere una delle costanti [AxisGroup](../../com.aspose.words/axisgroup/). |

### setBubbleScale(int value) {#setBubbleScale-int}
```
public void setBubbleScale(int value)
```


Imposta la dimensione delle bolle come percentuale della loro dimensione predefinita.

 **Remarks:** 

Si applica solo ai gruppi di serie del tipo [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE) e [ChartSeriesType.BUBBLE_3_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D).

L'intervallo di valori accettabili è da 0 a 300 inclusi. Il valore predefinito è 100.

 **Examples:** 

Mostra come impostare la dimensione delle bolle.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | La dimensione delle bolle in percentuale rispetto alla loro dimensione predefinita. |

### setDoughnutHoleSize(int value) {#setDoughnutHoleSize-int}
```
public void setDoughnutHoleSize(int value)
```


Imposta la dimensione del foro del grafico a ciambella principale come percentuale.

 **Remarks:** 

Si applica solo ai gruppi di serie del tipo [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT).

L'intervallo di valori accettabili è da 0 a 90 inclusi. Il valore predefinito è 75.

 **Examples:** 

Mostra come creare e formattare un grafico a ciambella.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | La dimensione del foro del grafico a ciambella principale in percentuale. |

### setFirstSliceAngle(int value) {#setFirstSliceAngle-int}
```
public void setFirstSliceAngle(int value)
```


Imposta l'angolo, in gradi, della prima fetta del grafico a torta principale.

 **Remarks:** 

Si applica ai gruppi di serie dei tipi [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D) e [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT).

L'intervallo di valori accettabili è da 0 a 360 inclusi. Il valore predefinito è 0.

 **Examples:** 

Mostra come creare e formattare un grafico a ciambella.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | L'angolo, in gradi, della prima fetta del grafico a torta principale. |

### setGapWidth(int value) {#setGapWidth-int}
```
public void setGapWidth(int value)
```


Imposta la percentuale della larghezza dello spazio tra gli elementi del grafico.

 **Remarks:** 

Si applica solo ai gruppi di serie dei tipi barra, colonna, pie-of-bar, pie-of-pie, histogram, box&whisker, waterfall e funnel.

L'intervallo di valori accettabili è da 0 a 500 inclusi. Per i gruppi di serie basati su barra/colonna, la proprietà rappresenta lo spazio tra i raggruppamenti di barre come percentuale della loro larghezza. Per i grafici pie-of-pie e bar-of-pie, questo è lo spazio tra le sezioni primaria e secondaria del grafico.

 **Examples:** 

Mostra come configurare la larghezza dello spazio e la sovrapposizione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | La percentuale di larghezza dello spazio tra gli elementi del grafico. |

### setOverlap(int value) {#setOverlap-int}
```
public void setOverlap(int value)
```


Imposta la percentuale di quanto le barre o le colonne della serie si sovrappongono.

 **Remarks:** 

Si applica ai gruppi di serie di tutti i tipi barra e colonna.

L'intervallo di valori accettabili è da -100 a 100 inclusi. Un valore di 0 indica che non c'è spazio tra le barre/colonne. Se il valore è -100, la distanza tra le barre/colonne è pari alla loro larghezza. Un valore di 100 significa che le barre/colonne si sovrappongono completamente.

 **Examples:** 

Mostra come configurare la larghezza dello spazio e la sovrapposizione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | La percentuale di sovrapposizione delle barre o colonne della serie. |

### setSecondSectionSize(int value) {#setSecondSectionSize-int}
```
public void setSecondSectionSize(int value)
```


Imposta la dimensione della sezione secondaria del grafico a torta come percentuale.

 **Remarks:** 

Si applica ai gruppi di serie dei tipi [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE) e [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR).

L'intervallo di valori accettabili è da 5 a 200 inclusi. Il valore predefinito è 75.

 **Examples:** 

Mostra come creare e formattare un grafico torta su torta.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | La dimensione della sezione secondaria del grafico a torta in percentuale. |

