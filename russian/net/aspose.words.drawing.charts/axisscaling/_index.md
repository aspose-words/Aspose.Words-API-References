---
title: Class AxisScaling
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.AxisScaling сорт. Представляет параметры масштабирования оси.
type: docs
weight: 560
url: /ru/net/aspose.words.drawing.charts/axisscaling/
---
## AxisScaling class

Представляет параметры масштабирования оси.

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
| [LogBase](../../aspose.words.drawing.charts/axisscaling/logbase/) { get; set; } | Получает или задает основание логарифма для логарифмической оси. |
| [Maximum](../../aspose.words.drawing.charts/axisscaling/maximum/) { get; set; } | Получает или задает максимальное значение оси. |
| [Minimum](../../aspose.words.drawing.charts/axisscaling/minimum/) { get; set; } | Получает или устанавливает минимальное значение оси. |
| [Type](../../aspose.words.drawing.charts/axisscaling/type/) { get; set; } | Получает или задает тип масштабирования оси. |

### Примеры

Показывает, как применить логарифмическое масштабирование к оси диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Очистить серию демонстрационных данных диаграммы, чтобы начать с чистой диаграммы.
chart.Series.Clear();

// Вставляем ряд с координатами X/Y для пяти точек.
chart.Series.Add("Series 1", 
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 }, 
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// Масштабирование оси X по умолчанию является линейным,
// отображение равномерно увеличивающихся значений, которые охватывают наш диапазон значений X (0, 1, 2, 3...).
// Линейная ось не идеальна для наших значений Y
// так как точки с меньшими значениями Y будет труднее читать.
// Логарифмическое масштабирование с основанием 20 (1, 20, 400, 8000...)
// разнесет нанесенные точки, что позволит нам легче читать их значения на графике.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)


