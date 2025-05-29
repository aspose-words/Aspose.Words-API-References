---
title: ChartSeries.CopyFormatFrom
linktitle: CopyFormatFrom
articleTitle: CopyFormatFrom
second_title: Aspose.Words para .NET
description: Descubra el método ChartSeries CopyFormatFrom para replicar sin esfuerzo formatos de puntos de datos por índice, mejorando la eficiencia y la consistencia de sus gráficos.
type: docs
weight: 190
url: /es/net/aspose.words.drawing.charts/chartseries/copyformatfrom/
---
## ChartSeries.CopyFormatFrom method

Copia el formato de punto de datos predeterminado del punto de datos con el índice especificado.

```csharp
public void CopyFormatFrom(int dataPointIndex)
```

## Ejemplos

Muestra cómo copiar el formato de puntos de datos.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

//Obtener el gráfico y la serie para actualizar el formato.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPointCollection dataPoints = series.DataPoints;

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsFalse(dataPoints.HasDefaultFormat(1));

// Copiar el formato del punto de datos con índice 1 al punto de datos con índice 2
// para que el punto de datos 2 se vea igual que el punto de datos 1.
dataPoints.CopyFormat(0, 1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

// Copiar el formato del punto de datos con índice 0 a los valores predeterminados de la serie para que todos los puntos de datos
// en la serie que tiene el formato predeterminado se ve igual que el punto de datos 0.
series.CopyFormatFrom(1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

doc.Save(ArtifactsDir + "Charts.CopyDataPointFormat.docx");
```

### Ver también

* class [ChartSeries](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
