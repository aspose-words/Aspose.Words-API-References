---
title: AxisScaling.LogBase
second_title: Справочник по API Aspose.Words для .NET
description: AxisScaling свойство. Получает или задает логарифмическое основание для логарифмической оси.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/axisscaling/logbase/
---
## AxisScaling.LogBase property

Получает или задает логарифмическое основание для логарифмической оси.

```csharp
public double LogBase { get; set; }
```

### Примечания

Это свойство не поддерживается новыми диаграммами MS Office 2016.

Допустимый диапазон значений с плавающей запятой больше или равен 2 и меньше или равен 1000. Свойство действует только в том случае, если[`Type`](../type/) установлено значение Logarithmic.

Установка этого свойства устанавливает[`Type`](../type/) собственностьLogarithmic .

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

* class [AxisScaling](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../axisscaling/)
* сборка [Aspose.Words](../../../)


