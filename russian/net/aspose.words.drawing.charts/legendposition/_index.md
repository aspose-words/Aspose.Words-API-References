---
title: LegendPosition Enum
linktitle: LegendPosition
articleTitle: LegendPosition
second_title: Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.LegendPosition перечисление. Указывает возможные положения легенды диаграммы на С#.
type: docs
weight: 910
url: /ru/net/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enumeration

Указывает возможные положения легенды диаграммы.

```csharp
public enum LegendPosition
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Для диаграммы легенда отображаться не будет. |
| Bottom | `1` | Указывает, что легенда должна отображаться внизу диаграммы. |
| Left | `2` | Указывает, что легенда должна отображаться слева от диаграммы. |
| Right | `3` | Указывает, что легенда должна отображаться справа от диаграммы. |
| Top | `4` | Указывает, что легенда должна отображаться в верхней части диаграммы. |
| TopRight | `5` | Указывает, что легенда должна отображаться в правом верхнем углу диаграммы. |

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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
