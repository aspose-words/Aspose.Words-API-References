---
title: Fill.PresetTextured
linktitle: PresetTextured
articleTitle: PresetTextured
second_title: Aspose.Words для .NET
description: Откройте для себя метод Fill PresetTextured, позволяющий с легкостью применять потрясающие предустановленные текстуры, придавая вашим проектам уникальную визуальную привлекательность.
type: docs
weight: 240
url: /ru/net/aspose.words.drawing/fill/presettextured/
---
## Fill.PresetTextured method

Устанавливает заливку на основе предустановленной текстуры.

```csharp
public void PresetTextured(PresetTexture presetTexture)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| presetTexture | PresetTexture | [`PresetTexture`](../../presettexture/) |

## Примеры

Покажите, как настроить форматирование маркера.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

// Удалить сгенерированную по умолчанию серию.
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

* enum [PresetTexture](../../presettexture/)
* class [Fill](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
