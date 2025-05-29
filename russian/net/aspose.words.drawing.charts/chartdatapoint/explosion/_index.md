---
title: ChartDataPoint.Explosion
linktitle: Explosion
articleTitle: Explosion
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartDataPoint Explosion для настройки точек данных круговой диаграммы. Управляйте движением из центра для эффектных визуализаций. Улучшите свои диаграммы сегодня!
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/chartdatapoint/explosion/
---
## ChartDataPoint.Explosion property

Указывает величину, на которую точка данных должна быть перемещена из центра круговой диаграммы. Может быть отрицательным; отрицательное значение означает, что свойство не задано и не должно применяться разбиение. Применяется только к круговым диаграммам.

```csharp
public int Explosion { get; set; }
```

## Примеры

Показывает, как перемещать сегменты круговой диаграммы от центра.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Pie, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Sales", chart.Series[0].Name);

// «Срезы» круговой диаграммы могут быть перемещены от центра на расстояние с помощью атрибута Explosion соответствующей точки данных.
// Добавьте точку данных в первую часть круговой диаграммы и сдвиньте ее от центра на 10 точек.
// Aspose.Words автоматически создает точки данных, если их не существует.
ChartDataPoint dataPoint = chart.Series[0].DataPoints[0];
dataPoint.Explosion = 10;

// Смещаем вторую часть на большее расстояние.
dataPoint = chart.Series[0].DataPoints[1];
dataPoint.Explosion = 40;

doc.Save(ArtifactsDir + "Charts.PieChartExplosion.docx");
```

### Смотрите также

* class [ChartDataPoint](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
