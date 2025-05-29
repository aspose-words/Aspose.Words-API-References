---
title: ChartSeriesGroup.GapWidth
linktitle: GapWidth
articleTitle: GapWidth
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartSeriesGroup GapWidth, позволяющее легко настроить процент зазора между элементами диаграммы для улучшенной визуализации данных.
type: docs
weight: 70
url: /ru/net/aspose.words.drawing.charts/chartseriesgroup/gapwidth/
---
## ChartSeriesGroup.GapWidth property

Возвращает или задает процент ширины зазора между элементами диаграммы.

```csharp
public int GapWidth { get; set; }
```

## Примечания

Применимо только к группам рядов типа «столбчатая диаграмма», «столбчатая диаграмма», «круговая диаграмма», «круговая диаграмма», «гистограмма», «ящик с усами», «водопад» и «воронка» .

Диапазон допустимых значений — от 0 до 500 включительно. Для групп рядов на основе столбцов/линий свойство представляет собой расстояние между кластерами столбцов в процентах от их ширины. Для круговых диаграмм и bar-of-pie это расстояние между первичной и вторичной секциями диаграммы.

## Примеры

Покажите, как настроить ширину зазора и перекрытие.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Устанавливаем ширину зазора между столбцами и перекрытие.
seriesGroup.GapWidth = 450;
seriesGroup.Overlap = -75;

doc.Save(ArtifactsDir + "Charts.ConfigureGapOverlap.docx");
```

### Смотрите также

* class [ChartSeriesGroup](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
