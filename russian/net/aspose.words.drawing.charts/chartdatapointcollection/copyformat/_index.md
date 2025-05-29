---
title: ChartDataPointCollection.CopyFormat
linktitle: CopyFormat
articleTitle: CopyFormat
second_title: Aspose.Words для .NET
description: Легко копируйте форматирование между точками данных с помощью метода ChartDataPointCollection CopyFormat. Улучшите визуализацию данных сегодня!
type: docs
weight: 40
url: /ru/net/aspose.words.drawing.charts/chartdatapointcollection/copyformat/
---
## ChartDataPointCollection.CopyFormat method

Копирует формат из исходной точки данных в целевую точку данных.

```csharp
public void CopyFormat(int sourceIndex, int destinationIndex)
```

## Примеры

Показывает, как копировать формат точки данных.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

// Получить диаграмму и ряд для обновления формата.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPointCollection dataPoints = series.DataPoints;

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsFalse(dataPoints.HasDefaultFormat(1));

// Копируем формат точки данных с индексом 1 в точку данных с индексом 2
// так что точка данных 2 выглядит так же, как точка данных 1.
dataPoints.CopyFormat(0, 1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

// Копируем формат точки данных с индексом 0 в значения по умолчанию для ряда, чтобы все точки данных
// в рядах, имеющих формат по умолчанию, выглядят так же, как точка данных 0.
series.CopyFormatFrom(1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

doc.Save(ArtifactsDir + "Charts.CopyDataPointFormat.docx");
```

### Смотрите также

* class [ChartDataPointCollection](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
