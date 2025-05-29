---
title: AxisDisplayUnit.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words para .NET
description: Descubra la propiedad AxisDisplayUnit, acceda fácilmente al documento vinculado a su gráfico principal para una gestión de datos perfecta y una visualización mejorada.
type: docs
weight: 30
url: /es/net/aspose.words.drawing.charts/axisdisplayunit/document/
---
## AxisDisplayUnit.Document property

Devuelve el documento que contiene el gráfico principal.

```csharp
public DocumentBase Document { get; }
```

## Ejemplos

Muestra cómo manipular las marcas de graduación y los valores mostrados de un eje de gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Establezca las marcas de graduación menores del eje Y para que apunten lejos del área de trazado,
// y las marcas de graduación principales cruzan el eje.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Establezca el eje Y para mostrar una marca principal cada 10 unidades y una marca secundaria cada 1 unidad.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Establezca los límites del eje Y en -10 y 20.
// Este eje Y ahora mostrará 4 marcas de graduación principales y 27 marcas de graduación secundarias.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// Para el eje X, establezca las marcas de graduación principales cada 10 unidades,
//cada marca de verificación menor en 2,5 unidades.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Configure ambos tipos de marcas de graduación para que aparezcan dentro del área de trazado del gráfico.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Establezca los límites del eje X de modo que éste abarque 5 marcas de graduación principales y 12 marcas de graduación secundarias.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabels.Alignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabels.Spacing);
Assert.AreEqual(doc, axis.DisplayUnit.Document);

// Establezca las etiquetas de verificación para mostrar su valor en millones.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

//Podemos establecer un valor más específico mediante el cual las etiquetas de marca mostrarán sus valores.
//Esta declaración es equivalente a la anterior.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Ver también

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [AxisDisplayUnit](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
