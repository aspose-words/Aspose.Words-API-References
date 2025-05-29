---
title: MarkerSymbol Enum
linktitle: MarkerSymbol
articleTitle: MarkerSymbol
second_title: Aspose.Words لـ .NET
description: استكشف مجموعة Aspose.Words.Drawing.Charts.MarkerSymbol للحصول على أنماط علامات قابلة للتخصيص تعمل على تحسين صور الرسم البياني لديك وتحسين عرض البيانات.
type: docs
weight: 1240
url: /ar/net/aspose.words.drawing.charts/markersymbol/
---
## MarkerSymbol enumeration

يحدد نمط رمز العلامة.

```csharp
public enum MarkerSymbol
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Default | `0` | يحدد رمز العلامة الافتراضي الذي سيتم رسمه عند كل نقطة بيانات. |
| Circle | `1` | يحدد أنه سيتم رسم دائرة عند كل نقطة بيانات. |
| Dash | `2` | يحدد أنه سيتم رسم شرطة عند كل نقطة بيانات. |
| Diamond | `3` | يحدد أنه سيتم رسم المعين في كل نقطة بيانات. |
| Dot | `4` | يحدد أنه سيتم رسم نقطة عند كل نقطة بيانات. |
| None | `5` | يحدد أنه لا يجب رسم أي شيء عند كل نقطة بيانات. |
| Picture | `6` | يحدد أنه سيتم رسم صورة عند كل نقطة بيانات. |
| Plus | `7` | يحدد أنه سيتم رسم علامة زائد عند كل نقطة بيانات. |
| Square | `8` | يحدد أنه سيتم رسم مربع عند كل نقطة بيانات. |
| Star | `9` | يحدد أنه سيتم رسم نجمة عند كل نقطة بيانات. |
| Triangle | `10` | يحدد المثلث الذي سيتم رسمه عند كل نقطة بيانات. |
| X | `11` | يحدد أنه سيتم رسم X عند كل نقطة بيانات. |

## أمثلة

يوضح كيفية العمل مع نقاط البيانات على مخطط خطي.

```csharp
public void ChartDataPoint()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape shape = builder.InsertChart(ChartType.Line, 500, 350);
    Chart chart = shape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // قم بالتأكيد على نقاط بيانات الرسم البياني من خلال جعلها تظهر على شكل أشكال ماسية.
    foreach (ChartSeries series in chart.Series)
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // قم بتنعيم الخط الذي يمثل سلسلة البيانات الأولى.
    chart.Series[0].Smooth = true;

    // تأكد من أن نقاط البيانات الخاصة بالسلسلة الأولى لن تعكس ألوانها إذا كانت القيمة سلبية.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    ChartDataPoint dataPoint = chart.Series[1].DataPoints[2];
    dataPoint.Format.Fill.Color = Color.Red;

    // للحصول على رسم بياني يبدو أكثر نظافة، يمكننا مسح التنسيق بشكل فردي.
    dataPoint.ClearFormat();

    // يمكننا أيضًا تجريد سلسلة كاملة من نقاط البيانات مرة واحدة.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// تطبيق عدد من نقاط البيانات على سلسلة.
/// </summary>
private static void ApplyDataPoints(ChartSeries series, int dataPointsCount, MarkerSymbol markerSymbol, int dataPointSize)
{
    for (int i = 0; i < dataPointsCount; i++)
    {
        ChartDataPoint point = series.DataPoints[i];
        point.Marker.Symbol = markerSymbol;
        point.Marker.Size = dataPointSize;

        Assert.AreEqual(i, point.Index);
    }
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
