---
title: ChartDataLabel
second_title: Справочник по API Aspose.Words для .NET
description: Представляет метку данных в точке диаграммы или линии тренда.
type: docs
weight: 630
url: /ru/net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

Представляет метку данных в точке диаграммы или линии тренда.

```csharp
public class ChartDataLabel
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index) { get; } | Указывает индекс содержащего элемента. Этот индекс должен определять, к какой из дочерних коллекций родителя относится этот элемент. Значение по умолчанию:0. |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden) { get; set; } | Получает/устанавливает флаг, указывающий, скрыта ли эта метка. Значение по умолчанию: **false** . |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible) { get; } | Возвращает true, если эта метка данных имеет что-то для отображения. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat) { get; } | Возвращает числовой формат родительского элемента. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator) { get; set; } | Получает или задает разделитель строк, используемый для меток данных на диаграмме. По умолчанию используется запятая, за исключением круговых диаграмм, показывающих только название категории и процентное соотношение, когда вместо нее должен использоваться разрыв строки . |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize) { get; set; } | Позволяет указать, должен ли размер пузырька отображаться для меток данных на графике. Применяется только к пузырьковым диаграммам. Значение по умолчанию — false. |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname) { get; set; } | Позволяет указать, будет ли отображаться название категории для меток данных на графике. Значение по умолчанию — false. |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange) { get; set; } | Позволяет указать, будут ли значения из диапазона меток данных отображаться в метках данных. Значение по умолчанию — false. |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines) { get; set; } | Позволяет указать, нужно ли отображать линии выноски меток данных. Значение по умолчанию — false. |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey) { get; set; } | Позволяет указать, должен ли отображаться ключ легенды для меток данных на графике. Значение по умолчанию — false. |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage) { get; set; } | Позволяет указать, следует ли отображать процентное значение для меток данных на графике. Значение по умолчанию — false. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname) { get; set; } | Возвращает или задает логическое значение, указывающее поведение отображения имени ряда для меток данных на диаграмме. True, чтобы показать название серии. Ложь скрывать. По умолчанию ложь. |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue) { get; set; } | Позволяет указать, должны ли значения отображаться в метках данных. Значение по умолчанию — false. |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat)() | Очищает формат этой метки данных. Для свойств устанавливаются значения по умолчанию, определенные в родительской коллекции данных label. |

### Примечания

В серииОбъектChartDataLabelявляется членом коллекции[`ChartDataLabelCollection`](../chartdatalabelcollection). Коллекция[`ChartDataLabelCollection`](../chartdatalabelcollection)содержит объект[`ChartDataLabel`](../chartdatalabel)для каждая точка.

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

* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
