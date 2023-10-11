---
title: Chart.Axes
second_title: Referencia de API de Aspose.Words para .NET
description: Chart propiedad. Obtiene una colección de todos los ejes de este gráfico.
type: docs
weight: 10
url: /es/net/aspose.words.drawing.charts/chart/axes/
---
## Chart.Axes property

Obtiene una colección de todos los ejes de este gráfico.

```csharp
public ChartAxisCollection Axes { get; }
```

### Ejemplos

Muestra cómo trabajar con la colección de ejes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;            

// Ocultar las líneas principales de la cuadrícula en los ejes Y primario y secundario.
foreach (ChartAxis axis in chart.Axes)
{
    if (axis.Type == ChartAxisType.Value)
        axis.HasMajorGridlines = false;
}

doc.Save(ArtifactsDir + "Charts.AxisCollection.docx");
```

### Ver también

* class [ChartAxisCollection](../../chartaxiscollection/)
* class [Chart](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../chart/)
* asamblea [Aspose.Words](../../../)


