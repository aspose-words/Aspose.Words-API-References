---
title: ChartDataLabel.ShowBubbleSize
linktitle: ShowBubbleSize
articleTitle: ShowBubbleSize
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ShowBubbleSize улучшает ваши пузырьковые диаграммы, отображая размеры меток данных. Оптимизируйте визуальное представление данных сегодня!
type: docs
weight: 130
url: /ru/net/aspose.words.drawing.charts/chartdatalabel/showbubblesize/
---
## ChartDataLabel.ShowBubbleSize property

Позволяет указать, следует ли отображать размер пузырьков для меток данных на диаграмме. Применимо только к пузырьковым диаграммам. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ShowBubbleSize { get; set; }
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

* class [ChartDataLabel](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
