---
title: "ChartSeriesGroup"
linktitle: "ChartSeriesGroup"
second_title: "Aspose.Words pour Java"
description: "Représente les propriétés d’un groupe de séries de graphique qui sont les propriétés des séries de même type associées aux mêmes axes en Java."
type: docs
weight: 87
url: /fr/java/com.aspose.words/chartseriesgroup/
---

**Inheritance:**
java.lang.Object
```
public class ChartSeriesGroup
```

Représente les propriétés d'un groupe de séries de graphique, c'est‑à‑dire les propriétés des séries de graphique du même type associées aux mêmes axes.

 **Remarks:** 

Les graphiques combinés contiennent plusieurs groupes de séries de graphique, avec un groupe distinct pour chaque type de série.

De plus, vous pouvez créer un groupe de séries de graphique pour assigner des axes secondaires à une ou plusieurs séries de graphique.

Pour en savoir plus, consultez l'article de documentation [ Working with Charts ][Working with Charts].

 **Examples:** 

Montre comment travailler avec l'axe secondaire du graphique.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getAxisGroup()](#getAxisGroup) | Obtient le groupe d'axes auquel appartient ce groupe de séries. |
| [getAxisX()](#getAxisX) | Fournit l'accès aux propriétés de l'axe X de ce groupe de séries. |
| [getAxisY()](#getAxisY) | Fournit l'accès aux propriétés de l'axe Y de ce groupe de séries. |
| [getBubbleScale()](#getBubbleScale) | Obtient la taille des bulles en pourcentage de leur taille par défaut. |
| [getDoughnutHoleSize()](#getDoughnutHoleSize) | Obtient la taille du trou du graphique en anneau parent en pourcentage. |
| [getFirstSliceAngle()](#getFirstSliceAngle) | Obtient l'angle, en degrés, de la première tranche du graphique circulaire parent. |
| [getGapWidth()](#getGapWidth) | Obtient le pourcentage de largeur d'écart entre les éléments du graphique. |
| [getOverlap()](#getOverlap) | Obtient le pourcentage de chevauchement des barres ou colonnes de séries. |
| [getSecondSectionSize()](#getSecondSectionSize) | Obtient la taille de la section secondaire du graphique circulaire en pourcentage. |
| [getSeries()](#getSeries) | Obtient une collection de séries appartenant à ce groupe de séries. |
| [getSeriesType()](#getSeriesType) | Obtient le type de séries de graphique incluses dans ce groupe. |
| [setAxisGroup(int value)](#setAxisGroup-int) | Définit le groupe d'axes auquel appartient ce groupe de séries. |
| [setBubbleScale(int value)](#setBubbleScale-int) | Définit la taille des bulles en pourcentage de leur taille par défaut. |
| [setDoughnutHoleSize(int value)](#setDoughnutHoleSize-int) | Définit la taille du trou du graphique en anneau parent en pourcentage. |
| [setFirstSliceAngle(int value)](#setFirstSliceAngle-int) | Définit l'angle, en degrés, de la première tranche du graphique circulaire parent. |
| [setGapWidth(int value)](#setGapWidth-int) | Définit le pourcentage de largeur d'écart entre les éléments du graphique. |
| [setOverlap(int value)](#setOverlap-int) | Définit le pourcentage de chevauchement des barres ou colonnes de séries. |
| [setSecondSectionSize(int value)](#setSecondSectionSize-int) | Définit la taille de la section secondaire du graphique circulaire en pourcentage. |
### getAxisGroup() {#getAxisGroup}
```
public int getAxisGroup()
```


Obtient le groupe d'axes auquel appartient ce groupe de séries.

 **Examples:** 

Montre comment travailler avec l'axe secondaire du graphique.

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
int - Le groupe d'axes auquel appartient ce groupe de séries. La valeur renvoyée est l'une des constantes [AxisGroup](../../com.aspose.words/axisgroup/).
### getAxisX() {#getAxisX}
```
public ChartAxis getAxisX()
```


Fournit l'accès aux propriétés de l'axe X de ce groupe de séries.

 **Examples:** 

Montre comment travailler avec l'axe secondaire du graphique.

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


Fournit l'accès aux propriétés de l'axe Y de ce groupe de séries.

 **Examples:** 

Montre comment travailler avec l'axe secondaire du graphique.

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


Obtient la taille des bulles en pourcentage de leur taille par défaut.

 **Remarks:** 

S'applique uniquement aux groupes de séries des types [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE) et [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D).

L'intervalle des valeurs acceptables va de 0 à 300 inclus. La valeur par défaut est 100.

 **Examples:** 

Montrez comment définir la taille des bulles.

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
int - La taille des bulles en pourcentage de leur taille par défaut.
### getDoughnutHoleSize() {#getDoughnutHoleSize}
```
public int getDoughnutHoleSize()
```


Obtient la taille du trou du graphique en anneau parent en pourcentage.

 **Remarks:** 

S'applique uniquement aux groupes de séries du type [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT).

L'intervalle des valeurs acceptables va de 0 à 90 inclus. La valeur par défaut est 75.

 **Examples:** 

Montre comment créer et formater un graphique en anneau.

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
int - La taille du trou du graphique en anneau parent en pourcentage.
### getFirstSliceAngle() {#getFirstSliceAngle}
```
public int getFirstSliceAngle()
```


Obtient l'angle, en degrés, de la première tranche du graphique circulaire parent.

 **Remarks:** 

S'applique aux groupes de séries des types [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D) et [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT) types.

L'intervalle des valeurs acceptables va de 0 à 360 inclus. La valeur par défaut est 0.

 **Examples:** 

Montre comment créer et formater un graphique en anneau.

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
int - L'angle, en degrés, de la première tranche du graphique circulaire parent.
### getGapWidth() {#getGapWidth}
```
public int getGapWidth()
```


Obtient le pourcentage de largeur d'écart entre les éléments du graphique.

 **Remarks:** 

S'applique uniquement aux groupes de séries des types barre, colonne, tarte‑sur‑barre, tarte‑sur‑tarte, histogramme, boîte‑et‑moustaches, cascade et entonnoir.

L'intervalle des valeurs acceptables va de 0 à 500 inclus. Pour les groupes de séries basés sur des barres/colonnes, la propriété représente l'espace entre les groupes de barres en pourcentage de leur largeur. Pour les graphiques tarte‑sur‑tarte et tarte‑sur‑barre, il s'agit de l'espace entre les sections principale et secondaire du graphique.

 **Examples:** 

Montre comment configurer la largeur des intervalles et le chevauchement.

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
int - Le pourcentage de largeur d'écart entre les éléments du graphique.
### getOverlap() {#getOverlap}
```
public int getOverlap()
```


Obtient le pourcentage de chevauchement des barres ou colonnes de séries.

 **Remarks:** 

S'applique aux groupes de séries de tous les types de barres et de colonnes.

L'intervalle des valeurs acceptables va de -100 à 100 inclus. Une valeur de 0 indique qu'il n'y a aucun espace entre les barres/colonnes. Si la valeur est -100, la distance entre les barres/colonnes est égale à leur largeur. Une valeur de 100 signifie que les barres/colonnes se chevauchent complètement.

 **Examples:** 

Montre comment configurer la largeur des intervalles et le chevauchement.

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
int - Le pourcentage du chevauchement des barres ou colonnes de la série.
### getSecondSectionSize() {#getSecondSectionSize}
```
public int getSecondSectionSize()
```


Obtient la taille de la section secondaire du graphique circulaire en pourcentage.

 **Remarks:** 

S'applique aux groupes de séries des types [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE) et [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR) types.

L'intervalle des valeurs acceptables va de 5 à 200 inclus. La valeur par défaut est 75.

 **Examples:** 

Montre comment créer et formater un graphique tarte‑sur‑tarte.

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
int - La taille de la section secondaire du graphique circulaire en pourcentage.
### getSeries() {#getSeries}
```
public ChartSeriesCollection getSeries()
```


Obtient une collection de séries appartenant à ce groupe de séries.

 **Examples:** 

Montre comment travailler avec l'axe secondaire du graphique.

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


Obtient le type de séries de graphique incluses dans ce groupe.

 **Examples:** 

Montre comment travailler avec l'axe secondaire du graphique.

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
int - Le type de série de graphique inclus dans ce groupe. La valeur retournée est l'une des constantes [ChartSeriesType](../../com.aspose.words/chartseriestype/) constants.
### setAxisGroup(int value) {#setAxisGroup-int}
```
public void setAxisGroup(int value)
```


Définit le groupe d'axes auquel appartient ce groupe de séries.

 **Examples:** 

Montre comment travailler avec l'axe secondaire du graphique.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Le groupe d'axes auquel appartient ce groupe de séries. La valeur doit être l'une des constantes [AxisGroup](../../com.aspose.words/axisgroup/) constants. |

### setBubbleScale(int value) {#setBubbleScale-int}
```
public void setBubbleScale(int value)
```


Définit la taille des bulles en pourcentage de leur taille par défaut.

 **Remarks:** 

S'applique uniquement aux groupes de séries des types [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE) et [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D).

L'intervalle des valeurs acceptables va de 0 à 300 inclus. La valeur par défaut est 100.

 **Examples:** 

Montrez comment définir la taille des bulles.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La taille des bulles en pourcentage de leur taille par défaut. |

### setDoughnutHoleSize(int value) {#setDoughnutHoleSize-int}
```
public void setDoughnutHoleSize(int value)
```


Définit la taille du trou du graphique en anneau parent en pourcentage.

 **Remarks:** 

S'applique uniquement aux groupes de séries du type [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT).

L'intervalle des valeurs acceptables va de 0 à 90 inclus. La valeur par défaut est 75.

 **Examples:** 

Montre comment créer et formater un graphique en anneau.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La taille du trou du graphique en anneau parent en pourcentage. |

### setFirstSliceAngle(int value) {#setFirstSliceAngle-int}
```
public void setFirstSliceAngle(int value)
```


Définit l'angle, en degrés, de la première tranche du graphique circulaire parent.

 **Remarks:** 

S'applique aux groupes de séries des types [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D) et [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT) types.

L'intervalle des valeurs acceptables va de 0 à 360 inclus. La valeur par défaut est 0.

 **Examples:** 

Montre comment créer et formater un graphique en anneau.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | L'angle, en degrés, de la première tranche du graphique circulaire parent. |

### setGapWidth(int value) {#setGapWidth-int}
```
public void setGapWidth(int value)
```


Définit le pourcentage de largeur d'écart entre les éléments du graphique.

 **Remarks:** 

S'applique uniquement aux groupes de séries des types barre, colonne, tarte‑sur‑barre, tarte‑sur‑tarte, histogramme, boîte‑et‑moustaches, cascade et entonnoir.

L'intervalle des valeurs acceptables va de 0 à 500 inclus. Pour les groupes de séries basés sur des barres/colonnes, la propriété représente l'espace entre les groupes de barres en pourcentage de leur largeur. Pour les graphiques tarte‑sur‑tarte et tarte‑sur‑barre, il s'agit de l'espace entre les sections principale et secondaire du graphique.

 **Examples:** 

Montre comment configurer la largeur des intervalles et le chevauchement.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Le pourcentage de largeur d'écart entre les éléments du graphique. |

### setOverlap(int value) {#setOverlap-int}
```
public void setOverlap(int value)
```


Définit le pourcentage de chevauchement des barres ou colonnes de séries.

 **Remarks:** 

S'applique aux groupes de séries de tous les types de barres et de colonnes.

L'intervalle des valeurs acceptables va de -100 à 100 inclus. Une valeur de 0 indique qu'il n'y a aucun espace entre les barres/colonnes. Si la valeur est -100, la distance entre les barres/colonnes est égale à leur largeur. Une valeur de 100 signifie que les barres/colonnes se chevauchent complètement.

 **Examples:** 

Montre comment configurer la largeur des intervalles et le chevauchement.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | Le pourcentage du chevauchement des barres ou colonnes de la série. |

### setSecondSectionSize(int value) {#setSecondSectionSize-int}
```
public void setSecondSectionSize(int value)
```


Définit la taille de la section secondaire du graphique circulaire en pourcentage.

 **Remarks:** 

S'applique aux groupes de séries des types [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE) et [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR) types.

L'intervalle des valeurs acceptables va de 5 à 200 inclus. La valeur par défaut est 75.

 **Examples:** 

Montre comment créer et formater un graphique tarte‑sur‑tarte.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La taille de la section secondaire du graphique circulaire en pourcentage. |

