---
title: ChartAxis.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartAxis Hidden para gestionar fácilmente la visibilidad de los ejes en sus gráficos. ¡Mejore la presentación de sus datos con esta sencilla función!
type: docs
weight: 110
url: /es/net/aspose.words.drawing.charts/chartaxis/hidden/
---
## ChartAxis.Hidden property

Obtiene o establece un indicador que indica si este eje está oculto o no.

```csharp
public bool Hidden { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO` .

## Ejemplos

Muestra cómo ocultar los ejes del gráfico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart.Series.Clear();

// Agregue una serie personalizada con categorías para el eje X y valores decimales respectivos para el eje Y.
chart.Series.Add("AW Series 1",
    new[] { "Item 1", "Item 2", "Item 3", "Item 4", "Item 5" },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2 });

 // Ocultar los ejes del gráfico para simplificar la apariencia del gráfico.
chart.AxisX.Hidden = true;
chart.AxisY.Hidden = true;

doc.Save(ArtifactsDir + "Charts.HideChartAxis.docx");
```

### Ver también

* class [ChartAxis](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
