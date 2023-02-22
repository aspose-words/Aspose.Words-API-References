---
title: Stroke.Visible
second_title: Справочник по API Aspose.Words для .NET
description: Stroke свойство. Получает или задает флаг указывающий виден ли штрих.
type: docs
weight: 190
url: /ru/net/aspose.words.drawing/stroke/visible/
---
## Stroke.Visible property

Получает или задает флаг, указывающий, виден ли штрих.

```csharp
public bool Visible { get; set; }
```

### Примечания

Значение по умолчанию для[`Shape`](../../shape/) является **истинный** .

### Примеры

Покажите, как настроить форматирование маркера.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

// Удалить созданную по умолчанию серию.
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// Установить форматирование маркера.
series.Marker.Size = 40;
series.Marker.Symbol = MarkerSymbol.Square;
ChartDataPointCollection dataPoints = series.DataPoints;
dataPoints[0].Marker.Format.Fill.PresetTextured(PresetTexture.Denim);
dataPoints[0].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[0].Marker.Format.Stroke.BackColor = Color.Red;
dataPoints[1].Marker.Format.Fill.PresetTextured(PresetTexture.WaterDroplets);
dataPoints[1].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[1].Marker.Format.Stroke.Visible = false;
dataPoints[2].Marker.Format.Fill.PresetTextured(PresetTexture.GreenMarble);
dataPoints[2].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[3].Marker.Format.Fill.PresetTextured(PresetTexture.Oak);
dataPoints[3].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[3].Marker.Format.Stroke.Transparency = 0.5;

doc.Save(ArtifactsDir + "Charts.MarkerFormatting.docx");
```

### Смотрите также

* class [Stroke](../)
* пространство имен [Aspose.Words.Drawing](../../stroke/)
* сборка [Aspose.Words](../../../)


