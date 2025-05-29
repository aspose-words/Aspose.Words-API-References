---
title: ChartSeries Class
linktitle: ChartSeries
articleTitle: ChartSeries
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Charts.ChartSeries — ваш ключ к улучшению свойств серий диаграмм для динамического создания и визуализации документов.
type: docs
weight: 1070
url: /ru/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

Представляет свойства ряда диаграмм.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) документальная статья.

```csharp
public class ChartSeries : IChartDataPoint
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } | Указывает, следует ли применять к пузырькам на пузырьковой диаграмме 3-D-эффект. |
| [BubbleSizes](../../aspose.words.drawing.charts/chartseries/bubblesizes/) { get; } | Получает коллекцию размеров пузырьков для этой серии диаграмм. |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | Задает настройки меток данных для всей серии. |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | Возвращает коллекцию объектов форматирования для всех точек данных в этой серии. |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } | Указывает величину, на которую точка данных должна быть перемещена из центра круговой диаграммы. Может быть отрицательным; отрицательное значение означает, что свойство не задано и не должно применяться разбиение. Применяется только к круговым диаграммам. |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | Предоставляет доступ к заполнению и форматированию линий серии. |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | Возвращает или задает флаг, указывающий, отображаются ли метки данных для серии. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } | Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное. |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | Получает запись легенды для этой серии диаграмм. |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } | Указывает маркер данных. Маркер создается автоматически при запросе. |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | Возвращает или задает имя серии, если имя не задано явно, оно генерируется с использованием индекса. По умолчанию возвращает серию плюс один основанный индекс. |
| [SeriesType](../../aspose.words.drawing.charts/chartseries/seriestype/) { get; } | Получает тип этой серии диаграмм. |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | Позволяет указать, будет ли линия, соединяющая точки на графике, сглажена с помощью сплайнов Катмулла-Рома. |
| [XValues](../../aspose.words.drawing.charts/chartseries/xvalues/) { get; } | Получает коллекцию значений X для этой серии диаграмм. |
| [YValues](../../aspose.words.drawing.charts/chartseries/yvalues/) { get; } | Получает коллекцию значений Y для этой серии диаграмм. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add)(*[ChartXValue](../chartxvalue/)*) | Добавляет указанное значение X к серии диаграмм. Если серия поддерживает значения Y и размеры пузырьков, они будут пустыми для значения X. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_1)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | Добавляет указанные значения X и Y в ряд диаграммы. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_2)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | Добавляет указанное значение X, значение Y и размер пузырька к серии диаграммы. |
| [Clear](../../aspose.words.drawing.charts/chartseries/clear/)() | Удаляет все значения данных из серии диаграмм. Формат всех отдельных точек данных и меток данных очищается. |
| [ClearValues](../../aspose.words.drawing.charts/chartseries/clearvalues/)() | Удаляет все значения данных из серии диаграммы с сохранением формата точек данных и меток данных. |
| [CopyFormatFrom](../../aspose.words.drawing.charts/chartseries/copyformatfrom/)(*int*) | Копирует формат точки данных по умолчанию из точки данных с указанным индексом. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert)(*int, [ChartXValue](../chartxvalue/)*) | Вставляет указанное значение X в ряд диаграммы по указанному индексу. Если ряд поддерживает значения Y и размеры пузырьков, они будут пустыми для значения X. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_1)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | Вставляет указанные значения X и Y в ряд диаграммы по указанному индексу. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_2)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | Вставляет указанное значение X, значение Y и размер пузырька в ряд диаграммы по указанному индексу. |
| [Remove](../../aspose.words.drawing.charts/chartseries/remove/)(*int*) | Удаляет значение X, значение Y и размер пузырька, если поддерживается, из серии диаграммы по указанному индексу. Соответствующая точка данных и метка данных также удаляются. |

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

* interface [IChartDataPoint](../ichartdatapoint/)
* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
