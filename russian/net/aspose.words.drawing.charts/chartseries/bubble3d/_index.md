---
title: ChartSeries.Bubble3D
linktitle: Bubble3D
articleTitle: Bubble3D
second_title: Aspose.Words для .NET
description: Улучшите свою пузырьковую диаграмму с помощью ChartSeries Bubble3D! Добавьте потрясающие 3D-эффекты к своим пузырькам для создания привлекательного визуального эффекта.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.charts/chartseries/bubble3d/
---
## ChartSeries.Bubble3D property

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

* class [ChartSeries](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
