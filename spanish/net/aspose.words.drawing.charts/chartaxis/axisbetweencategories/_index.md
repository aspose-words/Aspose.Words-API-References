---
title: ChartAxis.AxisBetweenCategories
linktitle: AxisBetweenCategories
articleTitle: AxisBetweenCategories
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartAxis AxisBetweenCategories: controle la posición del eje de valores para una mejor visualización de categorías en sus gráficos. ¡Optimice la presentación de sus datos!
type: docs
weight: 10
url: /es/net/aspose.words.drawing.charts/chartaxis/axisbetweencategories/
---
## ChartAxis.AxisBetweenCategories property

Obtiene o establece un indicador que indica si el eje de valores cruza el eje de categorías entre categorías.

```csharp
public bool AxisBetweenCategories { get; set; }
```

## Observaciones

La propiedad solo tiene efecto en ejes de valores. No es compatible con los nuevos gráficos de MS Office 2016.

## Ejemplos

Muestra cómo lograr que un eje de gráfico se cruce en una ubicación personalizada.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Para los gráficos de columnas, el eje Y se cruza en cero de manera predeterminada,
// lo que significa que las columnas para todos los valores por debajo de cero apuntan hacia abajo para representar valores negativos.
//Podemos establecer un valor diferente para el cruce del eje Y. En este caso, lo estableceremos en 3.
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### Ver también

* class [ChartAxis](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
