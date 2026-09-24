---
title: "ChartSeriesGroup"
linktitle: "ChartSeriesGroup"
second_title: "Aspose.Words para Java"
description: "Representa las propiedades de un grupo de series de gráfico que son las propiedades de series de gráfico del mismo tipo asociadas con los mismos ejes en Java."
type: docs
weight: 87
url: /es/java/com.aspose.words/chartseriesgroup/
---

**Inheritance:**
java.lang.Object
```
public class ChartSeriesGroup
```

Representa las propiedades de un grupo de series del gráfico, es decir, las propiedades de series del gráfico del mismo tipo asociadas a los mismos ejes.

 **Remarks:** 

Los gráficos combinados contienen múltiples grupos de series de gráfico, con un grupo separado para cada tipo de serie.

Además, puedes crear un grupo de series de gráfico para asignar ejes secundarios a una o más series de gráfico.

Para obtener más información, visite el artículo de documentación [ Working with Charts ][Working with Charts].

 **Examples:** 

Muestra cómo trabajar con el eje secundario del gráfico.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getAxisGroup()](#getAxisGroup) | Obtiene el grupo de ejes al que pertenece este grupo de series. |
| [getAxisX()](#getAxisX) | Proporciona acceso a las propiedades del eje X de este grupo de series. |
| [getAxisY()](#getAxisY) | Proporciona acceso a las propiedades del eje Y de este grupo de series. |
| [getBubbleScale()](#getBubbleScale) | Obtiene el tamaño de las burbujas como un porcentaje de su tamaño predeterminado. |
| [getDoughnutHoleSize()](#getDoughnutHoleSize) | Obtiene el tamaño del agujero del gráfico de rosquilla principal como un porcentaje. |
| [getFirstSliceAngle()](#getFirstSliceAngle) | Obtiene el ángulo, en grados, de la primera porción del gráfico circular principal. |
| [getGapWidth()](#getGapWidth) | Obtiene el porcentaje del ancho del espacio entre los elementos del gráfico. |
| [getOverlap()](#getOverlap) | Obtiene el porcentaje de cuánto se superponen las barras o columnas de la serie. |
| [getSecondSectionSize()](#getSecondSectionSize) | Obtiene el tamaño de la sección secundaria del gráfico circular como un porcentaje. |
| [getSeries()](#getSeries) | Obtiene una colección de series que pertenecen a este grupo de series. |
| [getSeriesType()](#getSeriesType) | Obtiene el tipo de serie de gráfico incluida en este grupo. |
| [setAxisGroup(int value)](#setAxisGroup-int) | Establece el grupo de ejes al que pertenece este grupo de series. |
| [setBubbleScale(int value)](#setBubbleScale-int) | Establece el tamaño de las burbujas como un porcentaje de su tamaño predeterminado. |
| [setDoughnutHoleSize(int value)](#setDoughnutHoleSize-int) | Establece el tamaño del agujero del gráfico de rosquilla principal como un porcentaje. |
| [setFirstSliceAngle(int value)](#setFirstSliceAngle-int) | Establece el ángulo, en grados, de la primera porción del gráfico circular principal. |
| [setGapWidth(int value)](#setGapWidth-int) | Establece el porcentaje del ancho del espacio entre los elementos del gráfico. |
| [setOverlap(int value)](#setOverlap-int) | Establece el porcentaje de cuánto se superponen las barras o columnas de la serie. |
| [setSecondSectionSize(int value)](#setSecondSectionSize-int) | Establece el tamaño de la sección secundaria del gráfico circular como un porcentaje. |
### getAxisGroup() {#getAxisGroup}
```
public int getAxisGroup()
```


Obtiene el grupo de ejes al que pertenece este grupo de series.

 **Examples:** 

Muestra cómo trabajar con el eje secundario del gráfico.

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
int - El grupo de ejes al que pertenece este grupo de series. El valor devuelto es una de las constantes [AxisGroup](../../com.aspose.words/axisgroup/).
### getAxisX() {#getAxisX}
```
public ChartAxis getAxisX()
```


Proporciona acceso a las propiedades del eje X de este grupo de series.

 **Examples:** 

Muestra cómo trabajar con el eje secundario del gráfico.

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


Proporciona acceso a las propiedades del eje Y de este grupo de series.

 **Examples:** 

Muestra cómo trabajar con el eje secundario del gráfico.

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


Obtiene el tamaño de las burbujas como un porcentaje de su tamaño predeterminado.

 **Remarks:** 

Se aplica solo a los grupos de series de los tipos [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE) y [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D).

El rango de valores aceptables es de 0 a 300 inclusive. El valor predeterminado es 100.

 **Examples:** 

Muestra cómo establecer el tamaño de las burbujas.

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
int - El tamaño de las burbujas como un porcentaje de su tamaño predeterminado.
### getDoughnutHoleSize() {#getDoughnutHoleSize}
```
public int getDoughnutHoleSize()
```


Obtiene el tamaño del agujero del gráfico de rosquilla principal como un porcentaje.

 **Remarks:** 

Se aplica solo a los grupos de series del tipo [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT).

El rango de valores aceptables es de 0 a 90 inclusive. El valor predeterminado es 75.

 **Examples:** 

Muestra cómo crear y formatear un gráfico de rosquilla.

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
int - El tamaño del agujero del gráfico de rosquilla principal como porcentaje.
### getFirstSliceAngle() {#getFirstSliceAngle}
```
public int getFirstSliceAngle()
```


Obtiene el ángulo, en grados, de la primera porción del gráfico circular principal.

 **Remarks:** 

Se aplica a los grupos de series de los tipos [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D) y [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT).

El rango de valores aceptables es de 0 a 360 inclusive. El valor predeterminado es 0.

 **Examples:** 

Muestra cómo crear y formatear un gráfico de rosquilla.

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
int - El ángulo, en grados, de la primera porción del gráfico circular principal.
### getGapWidth() {#getGapWidth}
```
public int getGapWidth()
```


Obtiene el porcentaje del ancho del espacio entre los elementos del gráfico.

 **Remarks:** 

Se aplica solo a los grupos de series de los tipos barra, columna, pastel-de-barra, pastel-de-pastel, histograma, caja y bigotes, cascada y embudo.

El rango de valores aceptables es de 0 a 500 inclusive. Para los grupos de series basados en barra/columna, la propiedad representa el espacio entre los grupos de barras como un porcentaje de su ancho. Para los gráficos pastel-de-pastel y barra-de-pastel, este es el espacio entre las secciones primaria y secundaria del gráfico.

 **Examples:** 

Muestra cómo configurar el ancho del espacio y la superposición.

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
int - El porcentaje del ancho del espacio entre los elementos del gráfico.
### getOverlap() {#getOverlap}
```
public int getOverlap()
```


Obtiene el porcentaje de cuánto se superponen las barras o columnas de la serie.

 **Remarks:** 

Se aplica a los grupos de series de todos los tipos de barra y columna.

El rango de valores aceptables es de -100 a 100 inclusive. Un valor de 0 indica que no hay espacio entre barras/columnas. Si el valor es -100, la distancia entre barras/columnas es igual a su ancho. Un valor de 100 significa que las barras/columnas se superponen completamente.

 **Examples:** 

Muestra cómo configurar el ancho del espacio y la superposición.

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
int - El porcentaje de cuánto se superponen las barras o columnas de la serie.
### getSecondSectionSize() {#getSecondSectionSize}
```
public int getSecondSectionSize()
```


Obtiene el tamaño de la sección secundaria del gráfico circular como un porcentaje.

 **Remarks:** 

Se aplica a los grupos de series de los tipos [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE) y [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR).

El rango de valores aceptables es de 5 a 200 inclusive. El valor predeterminado es 75.

 **Examples:** 

Muestra cómo crear y formatear un gráfico pastel de pastel.

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
int - El tamaño de la sección secundaria del gráfico pastel como porcentaje.
### getSeries() {#getSeries}
```
public ChartSeriesCollection getSeries()
```


Obtiene una colección de series que pertenecen a este grupo de series.

 **Examples:** 

Muestra cómo trabajar con el eje secundario del gráfico.

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


Obtiene el tipo de serie de gráfico incluida en este grupo.

 **Examples:** 

Muestra cómo trabajar con el eje secundario del gráfico.

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
int - El tipo de serie de gráfico incluido en este grupo. El valor devuelto es una de las constantes de [ChartSeriesType](../../com.aspose.words/chartseriestype/).
### setAxisGroup(int value) {#setAxisGroup-int}
```
public void setAxisGroup(int value)
```


Establece el grupo de ejes al que pertenece este grupo de series.

 **Examples:** 

Muestra cómo trabajar con el eje secundario del gráfico.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El grupo de ejes al que pertenece este grupo de series. El valor debe ser una de las constantes de [AxisGroup](../../com.aspose.words/axisgroup/). |

### setBubbleScale(int value) {#setBubbleScale-int}
```
public void setBubbleScale(int value)
```


Establece el tamaño de las burbujas como un porcentaje de su tamaño predeterminado.

 **Remarks:** 

Se aplica solo a los grupos de series de los tipos [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE) y [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D).

El rango de valores aceptables es de 0 a 300 inclusive. El valor predeterminado es 100.

 **Examples:** 

Muestra cómo establecer el tamaño de las burbujas.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El tamaño de las burbujas como porcentaje de su tamaño predeterminado. |

### setDoughnutHoleSize(int value) {#setDoughnutHoleSize-int}
```
public void setDoughnutHoleSize(int value)
```


Establece el tamaño del agujero del gráfico de rosquilla principal como un porcentaje.

 **Remarks:** 

Se aplica solo a los grupos de series del tipo [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT).

El rango de valores aceptables es de 0 a 90 inclusive. El valor predeterminado es 75.

 **Examples:** 

Muestra cómo crear y formatear un gráfico de rosquilla.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El tamaño del agujero del gráfico de rosquilla principal como porcentaje. |

### setFirstSliceAngle(int value) {#setFirstSliceAngle-int}
```
public void setFirstSliceAngle(int value)
```


Establece el ángulo, en grados, de la primera porción del gráfico circular principal.

 **Remarks:** 

Se aplica a los grupos de series de los tipos [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D) y [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT).

El rango de valores aceptables es de 0 a 360 inclusive. El valor predeterminado es 0.

 **Examples:** 

Muestra cómo crear y formatear un gráfico de rosquilla.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El ángulo, en grados, de la primera porción del gráfico circular principal. |

### setGapWidth(int value) {#setGapWidth-int}
```
public void setGapWidth(int value)
```


Establece el porcentaje del ancho del espacio entre los elementos del gráfico.

 **Remarks:** 

Se aplica solo a los grupos de series de los tipos barra, columna, pastel-de-barra, pastel-de-pastel, histograma, caja y bigotes, cascada y embudo.

El rango de valores aceptables es de 0 a 500 inclusive. Para los grupos de series basados en barra/columna, la propiedad representa el espacio entre los grupos de barras como un porcentaje de su ancho. Para los gráficos pastel-de-pastel y barra-de-pastel, este es el espacio entre las secciones primaria y secundaria del gráfico.

 **Examples:** 

Muestra cómo configurar el ancho del espacio y la superposición.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El porcentaje del ancho del espacio entre los elementos del gráfico. |

### setOverlap(int value) {#setOverlap-int}
```
public void setOverlap(int value)
```


Establece el porcentaje de cuánto se superponen las barras o columnas de la serie.

 **Remarks:** 

Se aplica a los grupos de series de todos los tipos de barra y columna.

El rango de valores aceptables es de -100 a 100 inclusive. Un valor de 0 indica que no hay espacio entre barras/columnas. Si el valor es -100, la distancia entre barras/columnas es igual a su ancho. Un valor de 100 significa que las barras/columnas se superponen completamente.

 **Examples:** 

Muestra cómo configurar el ancho del espacio y la superposición.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El porcentaje de cuánto se superponen las barras o columnas de la serie. |

### setSecondSectionSize(int value) {#setSecondSectionSize-int}
```
public void setSecondSectionSize(int value)
```


Establece el tamaño de la sección secundaria del gráfico circular como un porcentaje.

 **Remarks:** 

Se aplica a los grupos de series de los tipos [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE) y [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR).

El rango de valores aceptables es de 5 a 200 inclusive. El valor predeterminado es 75.

 **Examples:** 

Muestra cómo crear y formatear un gráfico pastel de pastel.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El tamaño de la sección secundaria del gráfico pastel como porcentaje. |

