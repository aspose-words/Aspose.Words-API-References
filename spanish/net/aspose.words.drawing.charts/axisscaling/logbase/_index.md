---
title: AxisScaling.LogBase
linktitle: LogBase
articleTitle: LogBase
second_title: Aspose.Words para .NET
description: Ajuste la base logarítmica de la propiedad AxisScaling LogBase para una visualización precisa de los datos y una mayor precisión gráfica. ¡Optimice sus gráficos hoy mismo!
type: docs
weight: 20
url: /es/net/aspose.words.drawing.charts/axisscaling/logbase/
---
## AxisScaling.LogBase property

Obtiene o establece la base logarítmica para un eje logarítmico.

```csharp
public double LogBase { get; set; }
```

## Observaciones

La propiedad no es compatible con los nuevos gráficos de MS Office 2016.

El rango válido de un valor de punto flotante es mayor o igual a 2 y menor o igual a 1000. La propiedad tiene efecto solo si[`Type`](../type/) se establece en Logarithmic.

Al establecer esta propiedad se establece el[`Type`](../type/) propiedad aLogarithmic .

## Ejemplos

Muestra cómo aplicar la escala logarítmica a un eje de gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

// Insertar una serie con coordenadas X/Y para cinco puntos.
chart.Series.Add("Series 1",
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 },
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// La escala del eje X es lineal por defecto,
// mostrando valores que se incrementan uniformemente y cubren nuestro rango de valores X (0, 1, 2, 3...).
// Un eje lineal no es ideal para nuestros valores Y
// ya que los puntos con valores Y más pequeños serán más difíciles de leer.
// Una escala logarítmica con base 20 (1, 20, 400, 8000...)
// distribuirá los puntos graficados, permitiéndonos leer sus valores en el gráfico más fácilmente.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Ver también

* class [AxisScaling](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
