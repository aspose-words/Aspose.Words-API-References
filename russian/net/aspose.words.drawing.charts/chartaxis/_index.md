---
title: Class ChartAxis
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartAxis сорт. Представляет параметры оси диаграммы.
type: docs
weight: 630
url: /ru/net/aspose.words.drawing.charts/chartaxis/
---
## ChartAxis class

Представляет параметры оси диаграммы.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) статья документации.

```csharp
public class ChartAxis
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [AxisBetweenCategories](../../aspose.words.drawing.charts/chartaxis/axisbetweencategories/) { get; set; } | Получает или задает флаг, указывающий, пересекает ли ось значений ось категорий между категориями. |
| [BaseTimeUnit](../../aspose.words.drawing.charts/chartaxis/basetimeunit/) { get; set; } | Возвращает или задает наименьшую единицу времени, представленную на оси категорий времени. |
| [CategoryType](../../aspose.words.drawing.charts/chartaxis/categorytype/) { get; set; } | Получает или задает тип оси категорий. |
| [Crosses](../../aspose.words.drawing.charts/chartaxis/crosses/) { get; set; } | Указывает, как эта ось пересекает перпендикулярную ось. |
| [CrossesAt](../../aspose.words.drawing.charts/chartaxis/crossesat/) { get; set; } | Указывает, где на перпендикулярной оси пересекается ось. |
| [DisplayUnit](../../aspose.words.drawing.charts/chartaxis/displayunit/) { get; } | Определяет значение масштабирования единиц отображения для оси значений. |
| [Document](../../aspose.words.drawing.charts/chartaxis/document/) { get; } | Возвращает документ, которому принадлежит правообладатель. |
| [HasMajorGridlines](../../aspose.words.drawing.charts/chartaxis/hasmajorgridlines/) { get; set; } | Получает или задает флаг, указывающий, есть ли на оси основные линии сетки. |
| [HasMinorGridlines](../../aspose.words.drawing.charts/chartaxis/hasminorgridlines/) { get; set; } | Получает или задает флаг, указывающий, есть ли на оси второстепенные линии сетки. |
| [Hidden](../../aspose.words.drawing.charts/chartaxis/hidden/) { get; set; } | Получает или устанавливает флаг, указывающий, скрыта эта ось или нет. |
| [MajorTickMark](../../aspose.words.drawing.charts/chartaxis/majortickmark/) { get; set; } | Возвращает или устанавливает основные деления. |
| [MajorUnit](../../aspose.words.drawing.charts/chartaxis/majorunit/) { get; set; } | Возвращает или устанавливает расстояние между основными делениями. |
| [MajorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/majorunitisauto/) { get; set; } | Получает или задает флаг, указывающий, следует ли использовать расстояние по умолчанию между основными делениями. |
| [MajorUnitScale](../../aspose.words.drawing.charts/chartaxis/majorunitscale/) { get; set; } | Возвращает или задает значение масштаба для основных делений на оси категории времени. |
| [MinorTickMark](../../aspose.words.drawing.charts/chartaxis/minortickmark/) { get; set; } | Возвращает или устанавливает второстепенные деления для оси. |
| [MinorUnit](../../aspose.words.drawing.charts/chartaxis/minorunit/) { get; set; } | Возвращает или устанавливает расстояние между второстепенными делениями. |
| [MinorUnitIsAuto](../../aspose.words.drawing.charts/chartaxis/minorunitisauto/) { get; set; } | Получает или задает флаг, указывающий, следует ли использовать расстояние по умолчанию между второстепенными делениями. |
| [MinorUnitScale](../../aspose.words.drawing.charts/chartaxis/minorunitscale/) { get; set; } | Возвращает или задает значение масштаба для второстепенных делений на оси категории времени. |
| [NumberFormat](../../aspose.words.drawing.charts/chartaxis/numberformat/) { get; } | Возвращает[`ChartNumberFormat`](../chartnumberformat/) объект, позволяющий определять числовые форматы для оси. |
| [ReverseOrder](../../aspose.words.drawing.charts/chartaxis/reverseorder/) { get; set; } | Возвращает или устанавливает флаг, указывающий, должны ли значения оси отображаться в обратном порядке, т.е. от максимума до минимума. |
| [Scaling](../../aspose.words.drawing.charts/chartaxis/scaling/) { get; } | Обеспечивает доступ к параметрам масштабирования оси. |
| [TickLabelAlignment](../../aspose.words.drawing.charts/chartaxis/ticklabelalignment/) { get; set; } | Получает или задает выравнивание текста меток деления оси. |
| [TickLabelOffset](../../aspose.words.drawing.charts/chartaxis/ticklabeloffset/) { get; set; } | Получает или задает расстояние меток от оси. |
| [TickLabelPosition](../../aspose.words.drawing.charts/chartaxis/ticklabelposition/) { get; set; } | Возвращает или задает положение меток делений на оси. |
| [TickLabelSpacing](../../aspose.words.drawing.charts/chartaxis/ticklabelspacing/) { get; set; } | Получает или задает интервал, с которым отрисовываются тиковые метки. |
| [TickLabelSpacingIsAuto](../../aspose.words.drawing.charts/chartaxis/ticklabelspacingisauto/) { get; set; } | Получает или задает флаг, указывающий, следует ли использовать автоматический интервал рисования меток делений. |
| [TickMarkSpacing](../../aspose.words.drawing.charts/chartaxis/tickmarkspacing/) { get; set; } | Получает или задает интервал, с которым рисуются деления. |
| [Title](../../aspose.words.drawing.charts/chartaxis/title/) { get; } | Предоставляет доступ к свойствам заголовка оси. |
| [Type](../../aspose.words.drawing.charts/chartaxis/type/) { get; } | Возвращает тип оси. |

### Примеры

Показывает, как вставить диаграмму и изменить внешний вид ее осей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Очистите ряд демонстрационных данных диаграммы, чтобы начать с чистой диаграммы.
chart.Series.Clear();

// Вставляем серию диаграмм с категориями для оси X и соответствующими числовыми значениями для оси Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Оси диаграммы имеют различные параметры, которые могут изменить их внешний вид,
// такие как их направление, такты основных/второстепенных единиц и деления.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabelOffset = 50;
xAxis.TickLabelPosition = AxisTickLabelPosition.Low;
xAxis.TickLabelSpacingIsAuto = false;
xAxis.TickMarkSpacing = 1;

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabelPosition = AxisTickLabelPosition.NextToAxis;

// Столбчатые диаграммы не имеют оси Z.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)


