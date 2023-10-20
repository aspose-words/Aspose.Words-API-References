---
title: ChartDataLabel Class
linktitle: ChartDataLabel
articleTitle: ChartDataLabel
second_title: Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartDataLabel сорт. Представляет метку данных на точке диаграммы или линии тренда на С#.
type: docs
weight: 670
url: /ru/net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

Представляет метку данных на точке диаграммы или линии тренда.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) статья документации.

```csharp
public class ChartDataLabel
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatalabel/font/) { get; } | Предоставляет доступ к форматированию шрифта этой метки данных. |
| [Format](../../aspose.words.drawing.charts/chartdatalabel/format/) { get; } | Предоставляет доступ к заполнению и форматированию строк метки данных. |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | Указывает индекс содержащего элемента. Этот индекс определяет, к какой из родительских дочерних коллекций относится этот элемент. Значение по умолчанию — 0. |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | Получает/устанавливает флаг, указывающий, скрыта ли эта метка. Значение по умолчанию:`ЛОЖЬ` . |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | Возвращает`истинный` если в этой метке данных есть что отображать. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | Возвращает числовой формат родительского элемента. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | Получает или задает разделитель строк, используемый для меток данных на диаграмме. По умолчанию используется запятая, за исключением круговых диаграмм, показывающих только имя категории и процентное соотношение, когда вместо этого должен использоваться разрыв строки . |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | Позволяет указать, должен ли отображаться размер пузырьков для меток данных на диаграмме. Применяется только к пузырьковым диаграммам. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | Позволяет указать, должно ли имя категории отображаться для меток данных на диаграмме. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | Позволяет указать, будут ли значения из диапазона меток данных отображаться в метках данных. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | Позволяет указать, нужно ли отображать выносные линии меток данных. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | Позволяет указать, должен ли отображаться ключ легенды для меток данных на диаграмме. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | Позволяет указать, будет ли отображаться процентное значение для меток данных на диаграмме. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | Возвращает или задает логическое значение, указывающее поведение отображения имени ряда для меток данных на диаграмме. `истинный` показать название серии;`ЛОЖЬ` прятаться. По умолчанию`ЛОЖЬ` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | Позволяет указать, должны ли значения отображаться в метках данных. Значение по умолчанию:`ЛОЖЬ` . |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | Очищает формат этой метки данных. Для свойств установлены значения по умолчанию, определенные в родительской коллекции меток data . . |

## Примечания

В сериале`ChartDataLabel` объект является членом[`ChartDataLabelCollection`](../chartdatalabelcollection/) . [`ChartDataLabelCollection`](../chartdatalabelcollection/) содержит`ChartDataLabel` объект для каждой точки.

## Примеры

Показывает, как применять метки к точкам данных на линейной диаграмме.

```csharp
public void DataLabels()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape chartShape = builder.InsertChart(ChartType.Line, 400, 300);
    Chart chart = chartShape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // Применяем метки данных к каждой серии диаграммы.
    // Эти метки появятся рядом с каждой точкой данных на графике и отобразят ее значение.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // Измените строку-разделитель для каждой метки данных в серии.
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.AreEqual(", ", enumerator.Current.Separator);
            enumerator.Current.Separator = " & ";
        }
    }

    // Чтобы график выглядел чище, мы можем удалить метки данных по отдельности.
    chart.Series[1].DataLabels[2].ClearFormat();

    // Мы также можем сразу удалить целую серию меток данных.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Примените метки данных с произвольным числовым форматом и разделителем к нескольким точкам данных в серии.
/// </summary>
private static void ApplyDataLabels(ChartSeries series, int labelsCount, string numberFormat, string separator)
{
    for (int i = 0; i < labelsCount; i++)
    {
        series.HasDataLabels = true;

        Assert.False(series.DataLabels[i].IsVisible);

        series.DataLabels[i].ShowCategoryName = true;
        series.DataLabels[i].ShowSeriesName = true;
        series.DataLabels[i].ShowValue = true;
        series.DataLabels[i].ShowLeaderLines = true;
        series.DataLabels[i].ShowLegendKey = true;
        series.DataLabels[i].ShowPercentage = false;
        series.DataLabels[i].IsHidden = false;
        Assert.False(series.DataLabels[i].ShowDataLabelsRange);

        series.DataLabels[i].NumberFormat.FormatCode = numberFormat;
        series.DataLabels[i].Separator = separator;

        Assert.False(series.DataLabels[i].ShowDataLabelsRange);
        Assert.True(series.DataLabels[i].IsVisible);
        Assert.False(series.DataLabels[i].IsHidden);
    }
}
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
