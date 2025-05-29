---
title: ChartAxis.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartAxis Hidden, чтобы легко управлять видимостью осей в ваших диаграммах. Улучшите представление данных с помощью этой простой функции переключения!
type: docs
weight: 110
url: /ru/net/aspose.words.drawing.charts/chartaxis/hidden/
---
## ChartAxis.Hidden property

Возвращает или задает флаг, указывающий, скрыта ли эта ось или нет.

```csharp
public bool Hidden { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` .

## Примеры

Показывает, как скрыть оси диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Очистите ряд демонстрационных данных диаграммы, чтобы начать с чистой диаграммы.
chart.Series.Clear();

// Добавьте пользовательскую серию с категориями для оси X и соответствующими десятичными значениями для оси Y.
chart.Series.Add("AW Series 1",
    new[] { "Item 1", "Item 2", "Item 3", "Item 4", "Item 5" },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2 });

 // Скройте оси диаграммы, чтобы упростить ее внешний вид.
chart.AxisX.Hidden = true;
chart.AxisY.Hidden = true;

doc.Save(ArtifactsDir + "Charts.HideChartAxis.docx");
```

### Смотрите также

* class [ChartAxis](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
