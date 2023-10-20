---
title: ChartDataLabelCollection Class
linktitle: ChartDataLabelCollection
articleTitle: ChartDataLabelCollection
second_title: Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartDataLabelCollection сорт. Представляет коллекциюChartDataLabel  на С#.
type: docs
weight: 680
url: /ru/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Представляет коллекцию[`ChartDataLabel`](../chartdatalabel/) .

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) статья документации.

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count/) { get; } | Возвращает количество[`ChartDataLabel`](../chartdatalabel/) в этой коллекции. |
| [Font](../../aspose.words.drawing.charts/chartdatalabelcollection/font/) { get; } | Предоставляет доступ к форматированию шрифта меток данных всей серии. |
| [Format](../../aspose.words.drawing.charts/chartdatalabelcollection/format/) { get; } | Предоставляет доступ к заполнению и форматированию строк меток данных. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item/) { get; } | Возвращает[`ChartDataLabel`](../chartdatalabel/) для указанного индекса. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat/) { get; } | Получает[`ChartNumberFormat`](../chartnumberformat/) экземпляр, позволяющий установить числовой формат для меток данных всей серии . |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator/) { get; set; } | Получает или задает разделитель строк, используемый для меток данных всей серии. По умолчанию используется запятая, за исключением круговых диаграмм, показывающих только имя категории и процентное соотношение, когда вместо этого должен использоваться разрыв строки . |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/) { get; set; } | Позволяет указать, должен ли отображаться размер пузырьков для меток данных всей серии. Применяется только к пузырьковым диаграммам. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/) { get; set; } | Позволяет указать, должно ли имя категории отображаться для меток данных всей серии. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/) { get; set; } | Позволяет указать, будут ли значения из диапазона меток данных отображаться в метках данных всей серии. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/) { get; set; } | Позволяет указать, нужно ли отображать выносные линии меток данных для меток данных всей серии. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/) { get; set; } | Позволяет указать, должен ли отображаться ключ легенды для меток данных всей серии. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/) { get; set; } | Позволяет указать, должно ли отображаться процентное значение для меток данных всей серии. Значение по умолчанию:`ЛОЖЬ` . Применяется только к круговым диаграммам. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/) { get; set; } | Возвращает или задает логическое значение, указывающее поведение отображения имени серии для меток данных всей серии. `истинный` показать название серии;`ЛОЖЬ` прятаться. По умолчанию`ЛОЖЬ` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue/) { get; set; } | Позволяет указать, должны ли значения отображаться в метках данных всей серии. Значение по умолчанию:`ЛОЖЬ` . |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat/)() | Очищает формат всех[`ChartDataLabel`](../chartdatalabel/) в этой коллекции. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator/)() | Возвращает объект перечислителя. |

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

* class [ChartDataLabel](../chartdatalabel/)
* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
