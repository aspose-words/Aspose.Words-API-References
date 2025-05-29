---
title: ChartLegend.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartLegend Position, которое позволит легко настроить размещение легенды вашей диаграммы для большей ясности и визуальной привлекательности.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing.charts/chartlegend/position/
---
## ChartLegend.Position property

Указывает положение легенды на диаграмме.

```csharp
public LegendPosition Position { get; set; }
```

## Примечания

Значение по умолчанию:Right для диаграмм до Word 2016 года and Top для диаграмм Word 2016.

## Примеры

Показывает, как редактировать внешний вид легенды диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Переместить легенду диаграммы в верхний правый угол.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Дайте другим элементам диаграммы, таким как график, больше места, разрешив им перекрывать легенду.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Смотрите также

* enum [LegendPosition](../../legendposition/)
* class [ChartLegend](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
