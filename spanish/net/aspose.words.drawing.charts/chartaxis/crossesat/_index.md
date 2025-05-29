---
title: ChartAxis.CrossesAt
linktitle: CrossesAt
articleTitle: CrossesAt
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartAxis CrossesAt para definir fácilmente puntos de intersección en el eje perpendicular de su gráfico para una mejor visualización de datos.
type: docs
weight: 50
url: /es/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

Especifica en qué punto del eje perpendicular se cruza el eje.

```csharp
public double CrossesAt { get; set; }
```

## Observaciones

La propiedad sólo tiene efecto si[`Crosses`](../crosses/) están configurados paraCustom. No es compatible con los nuevos gráficos de MS Office 2016.

Las unidades se determinan según el tipo de eje. Cuando se trata de un eje de valores, el valor de la propiedad es un número decimal. Cuando se trata de un eje de categorías temporales, el valor se define como , un número entero de días con respecto a la fecha base (30/12/1899). Para un eje de categorías de texto, el valor es , un número entero de categoría, comenzando con 1 como la primera categoría.

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
