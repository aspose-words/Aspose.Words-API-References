---
title: AxisScaling.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words для .NET
description: Откройте для себя свойство AxisScaling Type, чтобы легко настроить масштабирование осей. Улучшите визуализацию данных с помощью гибких настроек для оптимальной ясности.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing.charts/axisscaling/type/
---
## AxisScaling.Type property

Возвращает или задает тип масштабирования оси.

```csharp
public AxisScaleType Type { get; set; }
```

## Примечания

Linearзначение является единственным, которое разрешено в новых диаграммах MS Office 2016.

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

* enum [AxisScaleType](../../axisscaletype/)
* class [AxisScaling](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
