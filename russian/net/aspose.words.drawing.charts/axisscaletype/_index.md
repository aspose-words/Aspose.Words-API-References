---
title: Enum AxisScaleType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.AxisScaleType перечисление. Указывает возможные типы масштаба для оси.
type: docs
weight: 560
url: /ru/net/aspose.words.drawing.charts/axisscaletype/
---
## AxisScaleType enumeration

Указывает возможные типы масштаба для оси.

```csharp
public enum AxisScaleType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Linear | `0` | Линейное масштабирование. |
| Logarithmic | `1` | Логарифмическое масштабирование. |

### Примеры

Показывает, как применить логарифмическое масштабирование к оси диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Очистите ряд демонстрационных данных диаграммы, чтобы начать с чистой диаграммы.
chart.Series.Clear();

// Вставляем серию с координатами X/Y для пяти точек.
chart.Series.Add("Series 1", 
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 }, 
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// Масштабирование оси X по умолчанию линейное,
// отображение равномерно увеличивающихся значений, охватывающих наш диапазон значений X (0, 1, 2, 3...).
// Линейная ось не идеальна для наших значений Y
// так как точки с меньшими значениями Y будет труднее читать.
// Логарифмическое масштабирование с основанием 20 (1, 20, 400, 8000...)
// распределит нанесенные точки, что позволит нам легче читать их значения на графике.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)


