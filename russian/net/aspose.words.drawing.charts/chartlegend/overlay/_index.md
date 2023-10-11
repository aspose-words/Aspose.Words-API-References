---
title: ChartLegend.Overlay
second_title: Справочник по API Aspose.Words для .NET
description: ChartLegend свойство. Определяет разрешено ли другим элементам диаграммы перекрывать легенду. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.charts/chartlegend/overlay/
---
## ChartLegend.Overlay property

Определяет, разрешено ли другим элементам диаграммы перекрывать легенду. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool Overlay { get; set; }
```

### Примеры

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

* class [ChartLegend](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../chartlegend/)
* сборка [Aspose.Words](../../../)


