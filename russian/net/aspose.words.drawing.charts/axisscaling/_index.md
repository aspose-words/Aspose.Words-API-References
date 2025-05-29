---
title: AxisScaling Class
linktitle: AxisScaling
articleTitle: AxisScaling
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Charts.AxisScaling для настраиваемых параметров масштабирования осей, которые позволят вам без труда улучшить презентации диаграмм.
type: docs
weight: 820
url: /ru/net/aspose.words.drawing.charts/axisscaling/
---
## AxisScaling class

Представляет параметры масштабирования оси.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) документальная статья.

```csharp
public class AxisScaling
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [AxisScaling](axisscaling/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [LogBase](../../aspose.words.drawing.charts/axisscaling/logbase/) { get; set; } | Возвращает или задает логарифмическое основание для логарифмической оси. |
| [Maximum](../../aspose.words.drawing.charts/axisscaling/maximum/) { get; set; } | Получает или задает максимальное значение оси. |
| [Minimum](../../aspose.words.drawing.charts/axisscaling/minimum/) { get; set; } | Получает или задает минимальное значение оси. |
| [Type](../../aspose.words.drawing.charts/axisscaling/type/) { get; set; } | Возвращает или задает тип масштабирования оси. |

## Примеры

Показывает, как применить логарифмическое масштабирование к оси диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Очистите ряд демонстрационных данных диаграммы, чтобы начать с чистой диаграммы.
chart.Series.Clear();

// Вставить ряд с координатами X/Y для пяти точек.
chart.Series.Add("Series 1",
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 },
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// Масштабирование оси X по умолчанию линейное,
// отображаем равномерно увеличивающиеся значения, которые охватывают наш диапазон значений X (0, 1, 2, 3...).
// Линейная ось не идеальна для наших значений Y
// поскольку точки с меньшими значениями Y будет сложнее читать.
// Логарифмическое масштабирование с основанием 20 (1, 20, 400, 8000...)
// распределит нанесенные точки, что позволит нам легче читать их значения на графике.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
