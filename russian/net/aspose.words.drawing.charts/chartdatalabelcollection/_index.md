---
title: ChartDataLabelCollection Class
linktitle: ChartDataLabelCollection
articleTitle: ChartDataLabelCollection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.ChartDataLabelCollection для эффективного управления метками данных диаграммы. Улучшите визуальную привлекательность вашего документа сегодня!
type: docs
weight: 940
url: /ru/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Представляет собой коллекцию[`ChartDataLabel`](../chartdatalabel/) .

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) документальная статья.

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count/) { get; } | Возвращает количество[`ChartDataLabel`](../chartdatalabel/) в этой коллекции. |
| [Font](../../aspose.words.drawing.charts/chartdatalabelcollection/font/) { get; } | Предоставляет доступ к форматированию шрифта меток данных всей серии. |
| [Format](../../aspose.words.drawing.charts/chartdatalabelcollection/format/) { get; } | Предоставляет доступ к заполнению и форматированию строк меток данных. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item/) { get; } | Возврат[`ChartDataLabel`](../chartdatalabel/) для указанного индекса. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat/) { get; } | Получает[`ChartNumberFormat`](../chartnumberformat/) экземпляр, позволяющий задать числовой формат для меток данных всей серии x000d_. |
| [Orientation](../../aspose.words.drawing.charts/chartdatalabelcollection/orientation/) { get; set; } | Возвращает или задает ориентацию текста меток данных всей серии. |
| [Position](../../aspose.words.drawing.charts/chartdatalabelcollection/position/) { get; set; } | Возвращает или задает положение меток данных. |
| [Rotation](../../aspose.words.drawing.charts/chartdatalabelcollection/rotation/) { get; set; } | Возвращает или задает поворот меток данных всего ряда в градусах. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator/) { get; set; } | Возвращает или задает разделитель строк, используемый для меток данных всей серии. По умолчанию используется запятая, за исключением круговых диаграмм, показывающих только название категории и процент, когда вместо этого следует использовать разрыв строки . |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/) { get; set; } | Позволяет указать, следует ли отображать размер пузырьков для меток данных всей серии. Применяется только к пузырьковым диаграммам. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/) { get; set; } | Позволяет указать, будет ли отображаться имя категории для меток данных всей серии. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/) { get; set; } | Позволяет указать, будут ли значения из диапазона меток данных отображаться в метках данных всей серии. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/) { get; set; } | Позволяет указать, нужно ли отображать выносные линии меток данных для меток данных всей серии. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/) { get; set; } | Позволяет указать, будет ли отображаться ключ легенды для меток данных всей серии. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/) { get; set; } | Позволяет указать, следует ли отображать процентное значение для меток данных всей серии. Значение по умолчанию:`ЛОЖЬ` . Применимо только к круговым диаграммам. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/) { get; set; } | Возвращает или задает логическое значение, указывающее поведение отображения имени серии для меток данных всей серии. `истинный` показать название серии;`ЛОЖЬ` скрыть. По умолчанию`ЛОЖЬ` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue/) { get; set; } | Позволяет указать, будут ли значения отображаться в метках данных всей серии. Значение по умолчанию:`ЛОЖЬ` . |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat/)() | Очищает формат всего[`ChartDataLabel`](../chartdatalabel/) в этой коллекции. |
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

    // Применить метки данных к каждой серии на диаграмме.
    // Эти метки будут отображаться рядом с каждой точкой данных на графике и отображать ее значение.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // Измените строку разделителя для каждой метки данных в серии.
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.AreEqual(", ", enumerator.Current.Separator);
            enumerator.Current.Separator = " & ";
        }
    }

    ChartDataLabel dataLabel = chart.Series[1].DataLabels[2];
    dataLabel.Format.Fill.Color = Color.Red;

    // Для более четкого вида графика мы можем удалить метки данных по отдельности.
    dataLabel.ClearFormat();

    // Мы также можем удалить целую серию меток данных за один раз.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Применить метки данных с пользовательским числовым форматом и разделителем к нескольким точкам данных в серии.
/// </summary>
private static void ApplyDataLabels(ChartSeries series, int labelsCount, string numberFormat, string separator)
{
    series.HasDataLabels = true;
    series.Explosion = 40;

    for (int i = 0; i < labelsCount; i++)
    {
        Assert.False(series.DataLabels[i].IsVisible);

        series.DataLabels[i].ShowCategoryName = true;
        series.DataLabels[i].ShowSeriesName = true;
        series.DataLabels[i].ShowValue = true;
        series.DataLabels[i].ShowLeaderLines = true;
        series.DataLabels[i].ShowLegendKey = true;
        series.DataLabels[i].ShowPercentage = false;
        Assert.False(series.DataLabels[i].IsHidden);
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
