---
title: ChartStyle Enum
linktitle: ChartStyle
articleTitle: ChartStyle
second_title: Aspose.Words для .NET
description: Применяйте предопределенные стили диаграмм в Aspose.Words. Улучшайте визуальные эффекты с помощью перечисления ChartStyle для профессионального форматирования документов.
type: docs
weight: 1130
url: /ru/net/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enumeration

Задает предопределенные стили диаграммы.

```csharp
public enum ChartStyle
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Normal | `0` | Представляет стиль диаграммы по умолчанию. |
| Muted | `1` | Стиль с приглушенными цветами. |
| Saturated | `2` | Стиль с более насыщенными цветами. |
| Shaded | `3` | Стиль с затененными точками данных. |
| Flat | `4` | Стиль с плоскими точками данных без градиента. |
| Shadowed | `5` | Стиль с точками данных, имеющими тень. |
| Gradient | `6` | Стиль с градиентной заливкой точек данных. |
| Original | `7` | Стиль с оригинальным внешним видом диаграммы. |
| Transparent1 | `8` | Стиль с прозрачными точками данных. |
| Transparent2 | `9` | Стиль с прозрачными точками данных. |
| Outline | `10` | Стиль с точками данных, не имеющими заливки, а только контур. |
| OutlineBlack | `11` | Стиль с черным фоном диаграммы, в котором точки данных не имеют заливки, а только контур. |
| Black | `12` | Стиль с черным фоном диаграммы. |
| Grey | `13` | Стиль с серым градиентным фоном диаграммы. |
| Blue | `14` | Стиль с синим фоном диаграммы. |
| ShadedPlot | `15` | Стиль, в котором область графика затенена. |

## Примеры

Показывает, как задать и получить стиль диаграммы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем диаграмму в черном стиле.
builder.InsertChart(ChartType.Column, 400, 250, ChartStyle.Black);

doc.Save(ArtifactsDir + "Charts.SetChartStyle.docx");

doc = new Document(ArtifactsDir + "Charts.SetChartStyle.docx");

// Получить диаграмму для обновления.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;

// Получить стиль диаграммы.
Assert.AreEqual(ChartStyle.Black, chart.Style);
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
