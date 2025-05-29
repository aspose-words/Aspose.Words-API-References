---
title: ChartFormat.IsDefined
linktitle: IsDefined
articleTitle: IsDefined
second_title: Aspose.Words para .NET
description: Descubra si un formato está definido con la propiedad ChartFormat IsDefined. ¡Desbloquee hoy mismo un control de formato perfecto para sus gráficos!
type: docs
weight: 20
url: /es/net/aspose.words.drawing.charts/chartformat/isdefined/
---
## ChartFormat.IsDefined property

Obtiene una bandera que indica si hay algún formato definido.

```csharp
public bool IsDefined { get; }
```

## Ejemplos

Muestra cómo restablecer el relleno al valor predeterminado definido en la serie.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPoint dataPoint = series.DataPoints[1];

Assert.IsTrue(dataPoint.Format.IsDefined);

dataPoint.Format.SetDefaultFill();

doc.Save(ArtifactsDir + "Charts.ResetDataPointFill.docx");
```

### Ver también

* class [ChartFormat](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
