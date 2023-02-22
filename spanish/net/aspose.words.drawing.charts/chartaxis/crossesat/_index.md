---
title: ChartAxis.CrossesAt
second_title: Referencia de API de Aspose.Words para .NET
description: ChartAxis propiedad. Especifica dónde se cruza el eje en el eje perpendicular.
type: docs
weight: 50
url: /es/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

Especifica dónde se cruza el eje en el eje perpendicular.

```csharp
public double CrossesAt { get; set; }
```

### Observaciones

La propiedad tiene efecto sólo si[`Crosses`](../crosses/) están configurados paraCustom. No es compatible con los nuevos gráficos de MS Office 2016.

Las unidades vienen determinadas por el tipo de eje. Cuando el eje es un eje de valores, el valor de la propiedad es un número decimal en el eje de valores. Cuando el eje es un eje de categoría de tiempo, el valor se define como un número entero de días relativo a la fecha base (30/12/1899). Para un eje de categoría de texto, el valor es un número de categoría entero, comenzando con 1 como la primera categoría.

### Ejemplos

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

// Para gráficos de columnas, el eje Y cruza en cero por defecto,
// lo que significa que las columnas para todos los valores por debajo de cero apuntan hacia abajo para representar valores negativos.
// Podemos establecer un valor diferente para el cruce del eje Y. En este caso, lo estableceremos en 3.
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### Ver también

* class [ChartAxis](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../chartaxis/)
* asamblea [Aspose.Words](../../../)


