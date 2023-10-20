---
title: ChartAxis.CrossesAt
linktitle: CrossesAt
articleTitle: CrossesAt
second_title: Aspose.Words para .NET
description: ChartAxis CrossesAt propiedad. Especifica en qué parte del eje perpendicular se cruza el eje en C#.
type: docs
weight: 50
url: /es/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

Especifica en qué parte del eje perpendicular se cruza el eje.

```csharp
public double CrossesAt { get; set; }
```

## Observaciones

La propiedad sólo tiene efecto si[`Crosses`](../crosses/) están configurados paraCustom. No es compatible con los nuevos gráficos de MS Office 2016.

Las unidades vienen determinadas por el tipo de eje. Cuando el eje es un eje de valores, el valor de property es un número decimal en el eje de valores. Cuando el eje es un eje de categoría de tiempo, el valor se define como un número entero de días con respecto a la fecha base (30/12/1899). Para un eje de categorías de texto, el valor es un número de categoría entero, comenzando con 1 como primera categoría.

## Ejemplos

Muestra cómo hacer que un eje de gráfico se cruce en una ubicación personalizada.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Para gráficos de columnas, el eje Y cruza en cero de forma predeterminada,
// lo que significa que las columnas para todos los valores por debajo de cero apuntan hacia abajo para representar valores negativos.
// Podemos establecer un valor diferente para el cruce del eje Y. En este caso lo pondremos en 3.
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
