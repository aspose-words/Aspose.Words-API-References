---
title: ChartDataLabelCollection
second_title: Справочник по API Aspose.Words для .NET
description: Представляет наборChartDataLabel./chartdatalabel/ .
type: docs
weight: 640
url: /ru/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Представляет набор[`ChartDataLabel`](../chartdatalabel/) .

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count/) { get; } | Возвращает количество[`ChartDataLabel`](../chartdatalabel/) в этой коллекции. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item/) { get; } | Возвращает[`ChartDataLabel`](../chartdatalabel/) для указанного индекса. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat/) { get; } | Получает[`ChartNumberFormat`](../chartnumberformat/) экземпляр, позволяющий установить числовой формат для меток данных всей серии . |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator/) { get; set; } | Получает или задает разделитель строк, используемый для меток данных всего ряда. По умолчанию используется запятая, за исключением круговых диаграмм, показывающих только название категории и процентное соотношение, когда вместо этого следует использовать разрыв строки . |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/) { get; set; } | Позволяет указать, должен ли размер пузырька отображаться для меток данных всего ряда. Применяется только к пузырьковым диаграммам. Значение по умолчанию: **ЛОЖЬ** . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/) { get; set; } | Позволяет указать, будет ли отображаться имя категории для меток данных всей серии. Значение по умолчанию: **ЛОЖЬ** . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/) { get; set; } | Позволяет указать, будут ли значения из диапазона меток данных отображаться в метках данных всей серии. Значение по умолчанию: **ЛОЖЬ** . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/) { get; set; } | Позволяет указать, нужно ли отображать линии выноски меток данных для меток данных всей серии. Значение по умолчанию: **ЛОЖЬ** . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/) { get; set; } | Позволяет указать, должен ли отображаться ключ легенды для меток данных всей серии. Значение по умолчанию: **ЛОЖЬ** . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/) { get; set; } | Позволяет указать, будет ли отображаться процентное значение для меток данных всего ряда. Значение по умолчанию: **ЛОЖЬ** . Применяется только к круговым диаграммам. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/) { get; set; } | Возвращает или задает логическое значение, указывающее поведение отображения имени ряда для меток данных всего ряда.  **Истинный**чтобы показать название серии. **ЛОЖЬ** прятаться. По умолчанию **ЛОЖЬ** . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue/) { get; set; } | Позволяет указать, должны ли значения отображаться в метках данных всего ряда. Значение по умолчанию: **ЛОЖЬ** . |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat/)() | Очищает формат всех[`ChartDataLabel`](../chartdatalabel/) в этой коллекции. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator/)() | Возвращает объект перечислителя. |

### Примеры

Показывает, как применять метки к точкам данных на линейной диаграмме.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape chartShape = builder.InsertChart(ChartType.Line, 400, 300);
    Chart chart = chartShape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // Применяем метки данных к каждому ряду на диаграмме.
    // Эти метки будут отображаться рядом с каждой точкой данных на графике и отображать ее значение.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // Изменить строку-разделитель для каждой метки данных в серии.
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

    // Мы также можем сразу удалить целую серию его меток данных.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Применить метки данных с пользовательским числовым форматом и разделителем к нескольким точкам данных в ряду.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
