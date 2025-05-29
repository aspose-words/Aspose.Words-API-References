---
title: ChartFormat.SetDefaultFill
linktitle: SetDefaultFill
articleTitle: SetDefaultFill
second_title: Aspose.Words для .NET
description: Узнайте, как использовать метод ChartFormat SetDefaultFill, чтобы без труда восстановить исходное значение заливки элемента диаграммы по умолчанию.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing.charts/chartformat/setdefaultfill/
---
## ChartFormat.SetDefaultFill method

Сбрасывает заливку элемента диаграммы на значение по умолчанию.

```csharp
public void SetDefaultFill()
```

## Примеры

Показывает, как сбросить заливку до значения по умолчанию, определенного в серии.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPoint dataPoint = series.DataPoints[1];

Assert.IsTrue(dataPoint.Format.IsDefined);

dataPoint.Format.SetDefaultFill();

doc.Save(ArtifactsDir + "Charts.ResetDataPointFill.docx");
```

### Смотрите также

* class [ChartFormat](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
