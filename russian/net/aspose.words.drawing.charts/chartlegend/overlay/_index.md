---
title: ChartLegend.Overlay
linktitle: Overlay
articleTitle: Overlay
second_title: Aspose.Words для .NET
description: Элемент управления диаграммой перекрывается свойством ChartLegend Overlay. Улучшите визуализацию данных с помощью настраиваемых параметров легенды для более четкого понимания.
type: docs
weight: 40
url: /ru/net/aspose.words.drawing.charts/chartlegend/overlay/
---
## ChartLegend.Overlay property

Определяет, разрешено ли другим элементам диаграммы перекрывать легенду. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool Overlay { get; set; }
```

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

* class [ChartLegend](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
