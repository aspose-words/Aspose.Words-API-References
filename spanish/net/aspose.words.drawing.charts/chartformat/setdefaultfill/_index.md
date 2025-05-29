---
title: ChartFormat.SetDefaultFill
linktitle: SetDefaultFill
articleTitle: SetDefaultFill
second_title: Aspose.Words para .NET
description: Descubra cómo utilizar el método SetDefaultFill de ChartFormat para restaurar sin esfuerzo el relleno de su elemento gráfico a su valor predeterminado original.
type: docs
weight: 50
url: /es/net/aspose.words.drawing.charts/chartformat/setdefaultfill/
---
## ChartFormat.SetDefaultFill method

Restablece el relleno del elemento del gráfico para que tenga el valor predeterminado.

```csharp
public void SetDefaultFill()
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
