---
title: Chart.SeriesGroups
linktitle: SeriesGroups
articleTitle: SeriesGroups
second_title: Aspose.Words для .NET
description: Изучите свойство Chart SeriesGroups для легкого доступа к обширной коллекции групп рядов, что улучшит ваши возможности визуализации данных.
type: docs
weight: 90
url: /ru/net/aspose.words.drawing.charts/chart/seriesgroups/
---
## Chart.SeriesGroups property

Предоставляет доступ к коллекции групп серий этой диаграммы.

```csharp
public ChartSeriesGroupCollection SeriesGroups { get; }
```

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

* class [ChartSeriesGroupCollection](../../chartseriesgroupcollection/)
* class [Chart](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
