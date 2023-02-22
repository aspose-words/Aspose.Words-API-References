---
title: IChartDataPoint.Explosion
second_title: Referencia de API de Aspose.Words para .NET
description: IChartDataPoint propiedad. Especifica la cantidad que se moverá el punto de datos desde el centro del pastel. Puede ser negativo negativo significa que la propiedad no está establecida y no se debe aplicar ninguna explosión. Se aplica solo a gráficos circulares.
type: docs
weight: 20
url: /es/net/aspose.words.drawing.charts/ichartdatapoint/explosion/
---
## IChartDataPoint.Explosion property

Especifica la cantidad que se moverá el punto de datos desde el centro del pastel. Puede ser negativo, negativo significa que la propiedad no está establecida y no se debe aplicar ninguna explosión. Se aplica solo a gráficos circulares.

```csharp
public int Explosion { get; set; }
```

### Ejemplos

Muestra cómo alejar las porciones de un gráfico circular del centro.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Pie, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Sales", chart.Series[0].Name);

// Las "rebanadas" de un gráfico circular se pueden alejar del centro una distancia a través del atributo Explosión del punto de datos respectivo.
// Agregue un punto de datos a la primera parte del gráfico circular y aléjelo del centro 10 puntos.
// Aspose.Words crea puntos de datos automáticamente si no existen.
ChartDataPoint dataPoint = chart.Series[0].DataPoints[0];
dataPoint.Explosion = 10;

// Desplazar la segunda porción una distancia mayor.
dataPoint = chart.Series[0].DataPoints[1];
dataPoint.Explosion = 40;

doc.Save(ArtifactsDir + "Charts.PieChartExplosion.docx");
```

### Ver también

* interface [IChartDataPoint](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../ichartdatapoint/)
* asamblea [Aspose.Words](../../../)


