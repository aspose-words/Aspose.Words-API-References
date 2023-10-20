---
title: Chart.Legend
linktitle: Legend
articleTitle: Legend
second_title: Aspose.Words для .NET
description: Chart Legend свойство. Обеспечивает доступ к свойствам легенды диаграммы на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing.charts/chart/legend/
---
## Chart.Legend property

Обеспечивает доступ к свойствам легенды диаграммы.

```csharp
public ChartLegend Legend { get; }
```

## Примеры

Показывает, как изменить внешний вид легенды диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Перемещаем легенду диаграммы в правый верхний угол.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Дайте другим элементам диаграммы, таким как графику, больше места, разрешив им перекрывать легенду.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Смотрите также

* class [ChartLegend](../../chartlegend/)
* class [Chart](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
