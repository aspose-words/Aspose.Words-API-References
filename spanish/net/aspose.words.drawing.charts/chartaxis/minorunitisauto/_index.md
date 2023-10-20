---
title: ChartAxis.MinorUnitIsAuto
linktitle: MinorUnitIsAuto
articleTitle: MinorUnitIsAuto
second_title: Aspose.Words para .NET
description: ChartAxis MinorUnitIsAuto propiedad. Obtiene o establece una bandera que indica si se debe utilizar la distancia predeterminada entre marcas menores en C#.
type: docs
weight: 170
url: /es/net/aspose.words.drawing.charts/chartaxis/minorunitisauto/
---
## ChartAxis.MinorUnitIsAuto property

Obtiene o establece una bandera que indica si se debe utilizar la distancia predeterminada entre marcas menores.

```csharp
public bool MinorUnitIsAuto { get; set; }
```

## Observaciones

La propiedad tiene efecto para la categoría de tiempo y los ejes de valor.

## Ejemplos

Muestra cómo manipular las marcas y los valores mostrados de un eje de gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Establece las marcas menores del eje Y para que apunten en dirección opuesta al área de trazado,
// y las marcas principales para cruzar el eje.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Configure el eje Y para mostrar un tick mayor cada 10 unidades y un tick menor cada 1 unidad.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Establece los límites del eje Y en -10 y 20.
// Este eje Y ahora mostrará 4 marcas de graduación principales y 27 marcas de graduación menores.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// Para el eje X, establezca las marcas principales cada 10 unidades,
// cada marca menor en 2,5 unidades.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Configure ambos tipos de marcas para que aparezcan dentro del área de trazado del gráfico.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Establezca los límites del eje X de modo que el eje X abarque 5 marcas de graduación principales y 12 marcas de graduación menores.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabelAlignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabelSpacing);

// Establece las etiquetas de marca para mostrar su valor en millones.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Podemos establecer un valor más específico mediante el cual las etiquetas de marca mostrarán sus valores.
// Esta declaración es equivalente a la anterior.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Ver también

* class [ChartAxis](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
