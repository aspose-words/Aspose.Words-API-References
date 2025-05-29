---
title: ChartDataPoint.Explosion
linktitle: Explosion
articleTitle: Explosion
second_title: Aspose.Words para .NET
description: Descubra la propiedad ChartDataPoint Explosion para ajustar los puntos de datos de gráficos circulares. Controle el movimiento desde el centro para obtener visualizaciones impactantes. ¡Mejore sus gráficos hoy mismo!
type: docs
weight: 20
url: /es/net/aspose.words.drawing.charts/chartdatapoint/explosion/
---
## ChartDataPoint.Explosion property

Especifica la cantidad en que se moverá el punto de datos desde el centro del gráfico circular. Puede ser negativo; negativo significa que la propiedad no está configurada y no se debe aplicar ninguna explosión. Se aplica solo a gráficos circulares.

```csharp
public int Explosion { get; set; }
```

## Ejemplos

Muestra cómo mover las porciones de un gráfico circular lejos del centro.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Pie, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Sales", chart.Series[0].Name);

// Las "porciones" de un gráfico circular se pueden alejar del centro una distancia a través del atributo Explosión del punto de datos respectivo.
// Agregue un punto de datos a la primera parte del gráfico circular y muévalo 10 puntos lejos del centro.
// Aspose.Words crea puntos de datos automáticamente si no existen.
ChartDataPoint dataPoint = chart.Series[0].DataPoints[0];
dataPoint.Explosion = 10;

// Desplazar la segunda porción a una distancia mayor.
dataPoint = chart.Series[0].DataPoints[1];
dataPoint.Explosion = 40;

doc.Save(ArtifactsDir + "Charts.PieChartExplosion.docx");
```

### Ver también

* class [ChartDataPoint](../)
* espacio de nombres [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* asamblea [Aspose.Words](../../../)
