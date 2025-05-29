---
title: IChartDataPoint.Bubble3D
linktitle: Bubble3D
articleTitle: Bubble3D
second_title: Aspose.Words для .NET
description: Откройте для себя свойство IChartDataPoint Bubble3D, которое позволит улучшить пузырьковые диаграммы с помощью потрясающих 3D-эффектов для более захватывающей визуализации данных.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.charts/ichartdatapoint/bubble3d/
---
## IChartDataPoint.Bubble3D property

Указывает, следует ли применять к пузырькам на пузырьковой диаграмме 3-D-эффект.

```csharp
public bool Bubble3D { get; set; }
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

// Применить метку данных к каждому пузырьку, отображающую его диаметр.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Смотрите также

* interface [IChartDataPoint](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
