---
title: ChartFormat.IsDefined
linktitle: IsDefined
articleTitle: IsDefined
second_title: Aspose.Words для .NET
description: Узнайте, определен ли формат с помощью свойства ChartFormat IsDefined. Разблокируйте управление бесшовным форматированием для ваших диаграмм сегодня!
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/chartformat/isdefined/
---
## ChartFormat.IsDefined property

Получает флаг, указывающий, определен ли какой-либо формат.

```csharp
public bool IsDefined { get; }
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
