---
title: ChartSeries Class
linktitle: ChartSeries
articleTitle: ChartSeries
second_title: Aspose.Words для .NET
description: Aspose.Words.Drawing.Charts.ChartSeries сорт. Представляет свойства серии диаграмм на С#.
type: docs
weight: 780
url: /ru/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

Представляет свойства серии диаграмм.

Чтобы узнать больше, посетите[Работа с диаграммами](https://docs.aspose.com/words/net/working-with-charts/) статья документации.

```csharp
public class ChartSeries : IChartDataPoint
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } | Указывает, должен ли к пузырькам на пузырьковой диаграмме применяться трехмерный эффект. |
| [BubbleSizes](../../aspose.words.drawing.charts/chartseries/bubblesizes/) { get; } | Получает коллекцию размеров пузырьков для этой серии диаграмм. |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | Указывает настройки меток данных для всей серии. |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | Возвращает коллекцию объектов форматирования для всех точек данных в этой серии. |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } | Указывает, на сколько точка данных должна быть перемещена из центра круговой диаграммы. Может быть отрицательным. Отрицательное значение означает, что свойство не установлено и не следует применять развертывание. Применяется только к круговым диаграммам. |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | Предоставляет доступ к заливке и форматированию строк серии. |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | Получает или задает флаг, указывающий, отображаются ли метки данных для серии. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } | Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное. |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | Получает запись легенды для этой серии диаграмм. |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } | Указывает маркер данных. Маркер создается автоматически по запросу. |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | Получает или задает имя серии. Если имя не задано явно, оно генерируется с использованием индекса. По умолчанию возвращает серию плюс один индекс на основе индекса. |
| [SeriesType](../../aspose.words.drawing.charts/chartseries/seriestype/) { get; } | Получает тип этой серии диаграмм. |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | Позволяет указать, должна ли линия, соединяющая точки на диаграмме, сглаживаться с использованием сплайнов Catmull-Rom. |
| [XValues](../../aspose.words.drawing.charts/chartseries/xvalues/) { get; } | Получает коллекцию значений X для этой серии диаграмм. |
| [YValues](../../aspose.words.drawing.charts/chartseries/yvalues/) { get; } | Получает коллекцию значений Y для этой серии диаграмм. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add)(*[ChartXValue](../chartxvalue/)*) | Добавляет указанное значение X в серию диаграмм. Если серия поддерживает значения Y и размеры пузырьков, они будут пустыми для значения X. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_1)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | Добавляет указанные значения X и Y в серию диаграмм. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_2)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | Добавляет указанное значение X, значение Y и размер пузырька в серию диаграмм. |
| [Clear](../../aspose.words.drawing.charts/chartseries/clear/)() | Удаляет все значения данных из серии диаграмм. Формат всех отдельных точек данных и меток данных очищается. |
| [ClearValues](../../aspose.words.drawing.charts/chartseries/clearvalues/)() | Удаляет все значения данных из серии диаграмм с сохранением формата точек данных и меток данных. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert)(*int, [ChartXValue](../chartxvalue/)*) | Вставляет указанное значение X в серию диаграмм по указанному индексу. Если серия поддерживает значения Y и размеры пузырьков, они будут пустыми для значения X. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_1)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | Вставляет указанные значения X и Y в серию диаграмм по указанному индексу. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_2)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | Вставляет указанное значение X, значение Y и размер пузырька в серию диаграмм по указанному индексу. |
| [Remove](../../aspose.words.drawing.charts/chartseries/remove/)(*int*) | Удаляет значение X, значение Y и размер пузырька, если поддерживается, из серии диаграмм по указанному индексу. Соответствующая точка данных и метка данных также удаляются. |

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

* interface [IChartDataPoint](../ichartdatapoint/)
* пространство имен [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../)
