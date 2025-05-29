---
title: ChartAxis Class
linktitle: ChartAxis
articleTitle: ChartAxis
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Charts.ChartAxis для настраиваемых параметров осей диаграммы. Улучшите визуализацию данных без усилий!
type: docs
weight: 890
url: /ru/net/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class

Представляет параметры осей диаграммы.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) документальная статья.

```csharp
public class ChartAxis
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [AxisBetweenCategories](../../aspose.words.drawing.charts/chartaxis/axisbetweencategories/) { get; set; } | Возвращает или задает флаг, указывающий, пересекает ли ось значений ось категорий между категориями. |
| [BaseTimeUnit](../../aspose.words.drawing.charts/chartaxis/basetimeunit/) { get; set; } | Возвращает или задает наименьшую единицу времени, представленную на оси категории времени. |
| [CategoryType](../../aspose.words.drawing.charts/chartaxis/categorytype/) { get; set; } | Возвращает или задает тип оси категории. |
| [Crosses](../../aspose.words.drawing.charts/chartaxis/crosses/) { get; set; } | Указывает, как эта ось пересекает перпендикулярную ось. |
| [CrossesAt](../../aspose.words.drawing.charts/chartaxis/crossesat/) { get; set; } | Указывает, где на перпендикулярной оси пересекается ось. |
| [DisplayUnit](../../aspose.words.drawing.charts/chartaxis/displayunit/) { get; } | Указывает значение масштабирования единиц отображения для оси значений. |
| [Document](../../aspose.words.drawing.charts/chartaxis/document/) { get; } | Возвращает документ, содержащий родительскую диаграмму. |
| [Format](../../aspose.words.drawing.charts/chartaxis/format/) { get; } | Предоставляет доступ к форматированию линий осей и заполнению меток делений. |
| [HasMajorGridlines](../../aspose.words.drawing.charts/chartaxis/hasmajorgridlines/) { get; set; } | Возвращает или задает флаг, указывающий, имеет ли ось основные линии сетки. |
| [HasMinorGridlines](../../aspose.words.drawing.charts/chartaxis/hasminorgridlines/) { get; set; } | Возвращает или задает флаг, указывающий, имеет ли ось второстепенные линии сетки. |
| [Hidden](../../aspose.words.drawing.charts/chartaxis/hidden/) { get; set; } | Возвращает или задает флаг, указывающий, скрыта ли эта ось или нет. |
| [MajorTickMark](../../aspose.words.drawing.charts/chartaxis/majortickmark/) { get; set; } | Возвращает или устанавливает основные деления. |
| [MajorUnit](../../aspose.words.drawing.charts/chartaxis/majorunit/) { get; set; } | Возвращает или задает расстояние между основными делениями. |
| [MajorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/majorunitisauto/) { get; set; } | Возвращает или задает флаг, указывающий, следует ли использовать расстояние по умолчанию между основными делениями. |
| [MajorUnitScale](../../aspose.words.drawing.charts/chartaxis/majorunitscale/) { get; set; } | Возвращает или задает значение шкалы для основных делений на оси категории времени. |
| [MinorTickMark](../../aspose.words.drawing.charts/chartaxis/minortickmark/) { get; set; } | Возвращает или задает вспомогательные деления для оси. |
| [MinorUnit](../../aspose.words.drawing.charts/chartaxis/minorunit/) { get; set; } | Возвращает или задает расстояние между второстепенными делениями. |
| [MinorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/minorunitisauto/) { get; set; } | Возвращает или задает флаг, указывающий, следует ли использовать расстояние по умолчанию между второстепенными делениями. |
| [MinorUnitScale](../../aspose.words.drawing.charts/chartaxis/minorunitscale/) { get; set; } | Возвращает или задает значение шкалы для второстепенных делений на оси категорий времени. |
| [NumberFormat](../../aspose.words.drawing.charts/chartaxis/numberformat/) { get; } | Возвращает[`ChartNumberFormat`](../chartnumberformat/) объект, позволяющий определять числовые форматы для оси. |
| [ReverseOrder](../../aspose.words.drawing.charts/chartaxis/reverseorder/) { get; set; } | Возвращает или устанавливает флаг, указывающий, следует ли отображать значения оси в обратном порядке, т.е. от максимального значения к минимальному. |
| [Scaling](../../aspose.words.drawing.charts/chartaxis/scaling/) { get; } | Предоставляет доступ к параметрам масштабирования оси. |
| [TickLabels](../../aspose.words.drawing.charts/chartaxis/ticklabels/) { get; } | Предоставляет доступ к свойствам меток делений осей. |
| [TickMarkSpacing](../../aspose.words.drawing.charts/chartaxis/tickmarkspacing/) { get; set; } | Возвращает или задает интервал, с которым рисуются деления. |
| [Title](../../aspose.words.drawing.charts/chartaxis/title/) { get; } | Предоставляет доступ к свойствам заголовка оси. |
| [Type](../../aspose.words.drawing.charts/chartaxis/type/) { get; } | Возвращает тип оси. |

## Примеры

Показывает, как вставить диаграмму и изменить внешний вид ее осей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Очистите ряд демонстрационных данных диаграммы, чтобы начать с чистой диаграммы.
chart.Series.Clear();

// Вставьте ряд диаграмм с категориями для оси X и соответствующими числовыми значениями для оси Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Оси диаграммы имеют различные параметры, которые могут изменить их внешний вид,
// например, их направление, основные/дополнительные деления и отметки делений.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabels.Offset = 50;
xAxis.TickLabels.Position = AxisTickLabelPosition.Low;
xAxis.TickLabels.IsAutoSpacing = false;
xAxis.TickMarkSpacing = 1;

Assert.AreEqual(doc, xAxis.Document);

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabels.Position = AxisTickLabelPosition.NextToAxis;
yAxis.TickLabels.Alignment = ParagraphAlignment.Center;
yAxis.TickLabels.Font.Color = Color.Red;
yAxis.TickLabels.Spacing = 1;

// Столбчатые диаграммы не имеют оси Z.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
