---
title: ChartSeriesGroup.Overlap
linktitle: Overlap
articleTitle: Overlap
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartSeriesGroup Overlap, позволяющее легко настроить процент перекрытия полос или столбцов ряда для улучшенной визуализации данных.
type: docs
weight: 80
url: /ru/net/aspose.words.drawing.charts/chartseriesgroup/overlap/
---
## ChartSeriesGroup.Overlap property

Возвращает или задает процент перекрытия столбцов или полос ряда.

```csharp
public int Overlap { get; set; }
```

## Примечания

Применимо к группам серий всех типов стержней и столбцов.

Диапазон допустимых значений — от -100 до 100 включительно. Значение 0 указывает на отсутствие пространства между полосами/столбцами. Если значение равно -100, расстояние между полосами/столбцами равно их ширине. Значение 100 означает, что полосы/столбцы полностью перекрываются.

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
