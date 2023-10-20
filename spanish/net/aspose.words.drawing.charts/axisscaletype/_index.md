---
title: AxisScaleType Enum
linktitle: AxisScaleType
articleTitle: AxisScaleType
second_title: Aspose.Words para .NET
description: Aspose.Words.Drawing.Charts.AxisScaleType enumeración. Especifica los posibles tipos de escala para un eje en C#.
type: docs
weight: 560
url: /es/net/aspose.words.drawing.charts/axisscaletype/
---
## AxisScaleType enumeration

Especifica los posibles tipos de escala para un eje.

```csharp
public enum AxisScaleType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Linear | `0` | Escala lineal. |
| Logarithmic | `1` | Escalado logarítmico. |

## Ejemplos

Muestra cómo aplicar una escala logarítmica a un eje de gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Borra la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

// Inserta una serie con coordenadas X/Y para cinco puntos.
chart.Series.Add("Series 1", 
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 }, 
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// La escala del eje X es lineal por defecto,
// mostrando valores que se incrementan uniformemente y que cubren nuestro rango de valores X (0, 1, 2, 3...).
// Un eje lineal no es ideal para nuestros valores Y
// ya que los puntos con valores Y más pequeños serán más difíciles de leer.
// Una escala logarítmica con base 20 (1, 20, 400, 8000...)
// distribuirá los puntos trazados, permitiéndonos leer sus valores en el gráfico más fácilmente.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../)
