---
title: AxisDisplayUnit Class
linktitle: AxisDisplayUnit
articleTitle: AxisDisplayUnit
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.Charts.AxisDisplayUnit para personalizar las opciones de escala del eje de valores para mejorar la claridad y precisión de los gráficos.
type: docs
weight: 790
url: /es/net/aspose.words.drawing.charts/axisdisplayunit/
---
## AxisDisplayUnit class

Proporciona acceso a las opciones de escala de las unidades de visualización para el eje de valores.

Para obtener más información, visite el[Trabajar con gráficos](https://docs.aspose.com/words/net/working-with-charts/) Artículo de documentación.

```csharp
public class AxisDisplayUnit
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [AxisDisplayUnit](axisdisplayunit/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CustomUnit](../../aspose.words.drawing.charts/axisdisplayunit/customunit/) { get; set; } | Obtiene o establece un divisor definido por el usuario para escalar las unidades de visualización en el eje de valores. |
| [Document](../../aspose.words.drawing.charts/axisdisplayunit/document/) { get; } | Devuelve el documento que contiene el gráfico principal. |
| [Unit](../../aspose.words.drawing.charts/axisdisplayunit/unit/) { get; set; } | Obtiene o establece el valor de escala de las unidades de visualización como uno de los valores predefinidos. |

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

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
