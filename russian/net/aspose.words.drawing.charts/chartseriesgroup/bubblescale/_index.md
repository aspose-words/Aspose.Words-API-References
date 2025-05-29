---
title: ChartSeriesGroup.BubbleScale
linktitle: BubbleScale
articleTitle: BubbleScale
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartSeriesGroup BubbleScale, позволяющее настраивать размеры пузырьков на диаграммах, улучшая визуализацию данных и взаимодействие с пользователем.
type: docs
weight: 40
url: /ru/net/aspose.words.drawing.charts/chartseriesgroup/bubblescale/
---
## ChartSeriesGroup.BubbleScale property

Возвращает или задает размер пузырьков в процентах от их размера по умолчанию.

```csharp
public int BubbleScale { get; set; }
```

## Примечания

Применимо только к группам серийBubble и Bubble3D типы.

Диапазон допустимых значений — от 0 до 300 включительно. Значение по умолчанию — 100.

## Примеры

Покажите, как задать размер пузырьков.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте пузырьковую 3D-диаграмму.
Shape shape = builder.InsertChart(ChartType.Bubble3D, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Установить масштаб пузырьков на 200%.
seriesGroup.BubbleScale = 200;

doc.Save(ArtifactsDir + "Charts.BubbleScale.docx");
```

### Смотрите также

* class [ChartSeriesGroup](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
