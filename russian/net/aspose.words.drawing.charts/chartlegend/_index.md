---
title: ChartLegend Class
linktitle: ChartLegend
articleTitle: ChartLegend
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Charts.ChartLegend, чтобы улучшить ваши диаграммы с помощью настраиваемых свойств легенды для лучшей визуализации данных.
type: docs
weight: 1010
url: /ru/net/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class

Представляет свойства легенды диаграммы.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) документальная статья.

```csharp
public class ChartLegend
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegend/font/) { get; } | Предоставляет доступ к форматированию шрифта по умолчанию для записей легенды. Чтобы переопределить форматирование шрифта для конкретной записи легенды, используйте[`Font`](../chartlegendentry/font/) свойство. |
| [Format](../../aspose.words.drawing.charts/chartlegend/format/) { get; } | Предоставляет доступ к заполнению и форматированию линий легенды. |
| [LegendEntries](../../aspose.words.drawing.charts/chartlegend/legendentries/) { get; } | Возвращает коллекцию записей легенды для всех серий и линий тренда родительской диаграммы. |
| [Overlay](../../aspose.words.drawing.charts/chartlegend/overlay/) { get; set; } | Определяет, разрешено ли другим элементам диаграммы перекрывать легенду. Значение по умолчанию:`ЛОЖЬ` . |
| [Position](../../aspose.words.drawing.charts/chartlegend/position/) { get; set; } | Указывает положение легенды на диаграмме. |

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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
