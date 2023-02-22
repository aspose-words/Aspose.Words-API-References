---
title: ChartAxis.MajorUnitScale
second_title: Referencia de API de Aspose.Words para .NET
description: ChartAxis propiedad. Devuelve o establece el valor de escala para las principales marcas en el eje de categoría de tiempo.
type: docs
weight: 120
url: /es/net/aspose.words.drawing.charts/chartaxis/majorunitscale/
---
## ChartAxis.MajorUnitScale property

Devuelve o establece el valor de escala para las principales marcas en el eje de categoría de tiempo.

```csharp
public AxisTimeUnit MajorUnitScale { get; set; }
```

### Observaciones

La propiedad tiene efecto solo para ejes de categoría de tiempo.

### Ejemplos

Muestra cómo manipular las marcas de verificación y los valores mostrados de un eje de gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Establezca las marcas de verificación menores del eje Y para que apunten lejos del área de trazado,
// y las marcas principales para cruzar el eje.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Establece el eje Y para mostrar un tick mayor cada 10 unidades y un tick menor cada 1 unidad.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Establecer los límites del eje Y en -10 y 20.
// Este eje Y ahora mostrará 4 marcas principales y 27 marcas secundarias.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// Para el eje X, establezca las marcas principales cada 10 unidades,
// cada marca de verificación menor a 2,5 unidades.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Configure ambos tipos de marcas de verificación para que aparezcan dentro del área de trazado del gráfico.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Establecer los límites del eje X para que el eje X abarque 5 marcas principales y 12 marcas secundarias.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabelAlignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabelSpacing);

// Establecer las etiquetas de marca para mostrar su valor en millones.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Podemos establecer un valor más específico por el cual las etiquetas de marca mostrarán sus valores.
// Esta declaración es equivalente a la anterior.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Ver también

* enum [AxisTimeUnit](../../axistimeunit/)
* class [ChartAxis](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../chartaxis/)
* asamblea [Aspose.Words](../../../)


