---
title: Class ChartLegend
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartLegend сорт. Представляет свойства легенды диаграммы.
type: docs
weight: 720
url: /ru/net/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class

Представляет свойства легенды диаграммы.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) статья документации.

```csharp
public class ChartLegend
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [LegendEntries](../../aspose.words.drawing.charts/chartlegend/legendentries/) { get; } | Возвращает коллекцию записей легенды для всех рядов и линий тренда родительской диаграммы. |
| [Overlay](../../aspose.words.drawing.charts/chartlegend/overlay/) { get; set; } | Определяет, разрешено ли другим элементам диаграммы перекрывать легенду. Значение по умолчанию:`ЛОЖЬ` . |
| [Position](../../aspose.words.drawing.charts/chartlegend/position/) { get; set; } | Указывает положение легенды на диаграмме. Значение по умолчанию:Right . |

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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)


