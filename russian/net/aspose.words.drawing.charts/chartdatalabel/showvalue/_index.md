---
title: ChartDataLabel.ShowValue
linktitle: ShowValue
articleTitle: ShowValue
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChartDataLabel ShowValue для улучшения визуализации данных. Управляйте отображением значений в метках для более четкого понимания. По умолчанию — false.
type: docs
weight: 200
url: /ru/net/aspose.words.drawing.charts/chartdatalabel/showvalue/
---
## ChartDataLabel.ShowValue property

Позволяет указать, следует ли отображать значения в метках данных. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ShowValue { get; set; }
```

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

* class [ChartDataLabel](../)
* пространство имен [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* сборка [Aspose.Words](../../../)
