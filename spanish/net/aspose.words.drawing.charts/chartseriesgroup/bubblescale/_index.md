---
title: ChartSeriesGroup.BubbleScale
linktitle: BubbleScale
articleTitle: BubbleScale
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartSeriesGroup BubbleScale para personalizar los tamaños de las burbujas en sus gráficos, mejorando la visualización de datos y la participación del usuario.
type: docs
weight: 40
url: /es/net/aspose.words.drawing.charts/chartseriesgroup/bubblescale/
---
## ChartSeriesGroup.BubbleScale property

Obtiene o establece el tamaño de las burbujas como un porcentaje de su tamaño predeterminado.

```csharp
public int BubbleScale { get; set; }
```

## Observaciones

Se aplica únicamente a grupos de series de laBubble y Bubble3D tipos.

El rango de valores aceptables va de 0 a 300 inclusive. El valor predeterminado es 100.

## Ejemplos

Muestra cómo configurar el tamaño de las burbujas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar un gráfico de burbujas 3D.
Shape shape = builder.InsertChart(ChartType.Bubble3D, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Establezca la escala de burbuja al 200%.
seriesGroup.BubbleScale = 200;

doc.Save(ArtifactsDir + "Charts.BubbleScale.docx");
```

### Ver también

* class [ChartSeriesGroup](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
