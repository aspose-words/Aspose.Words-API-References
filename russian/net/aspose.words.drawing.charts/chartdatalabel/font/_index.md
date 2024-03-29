---
title: ChartDataLabel.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words для .NET
description: ChartDataLabel Font свойство. Предоставляет доступ к форматированию шрифта этой метки данных на С#.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.charts/chartdatalabel/font/
---
## ChartDataLabel.Font property

Предоставляет доступ к форматированию шрифта этой метки данных.

```csharp
public Font Font { get; }
```

## Примеры

Показывает, как использовать 3D-эффекты с пузырьковыми диаграммами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Применяем метку данных к каждому пузырьку, отображающую его диаметр.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Смотрите также

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabel](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
