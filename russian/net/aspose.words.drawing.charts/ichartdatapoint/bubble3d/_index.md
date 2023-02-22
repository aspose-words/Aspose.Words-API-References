---
title: IChartDataPoint.Bubble3D
second_title: Справочник по API Aspose.Words для .NET
description: IChartDataPoint свойство. Указывает следует ли применять к пузырькам в пузырьковой диаграмме трехмерный эффект.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.charts/ichartdatapoint/bubble3d/
---
## IChartDataPoint.Bubble3D property

Указывает, следует ли применять к пузырькам в пузырьковой диаграмме трехмерный эффект.

```csharp
public bool Bubble3D { get; set; }
```

### Примеры

Показывает, как использовать 3D-эффекты с пузырьковыми диаграммами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Применяем метку данных к каждому пузырьку, отображающему его диаметр.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Смотрите также

* interface [IChartDataPoint](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../ichartdatapoint/)
* сборка [Aspose.Words](../../../)


