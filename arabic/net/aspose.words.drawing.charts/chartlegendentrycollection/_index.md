---
title: ChartLegendEntryCollection Class
linktitle: ChartLegendEntryCollection
articleTitle: ChartLegendEntryCollection
second_title: Aspose.Words لـ .NET
description: استكشف Aspose.Words.ChartLegendEntryCollection لإدارة إدخالات أسطورة الرسم البياني بكفاءة وتحسين العروض التوضيحية للمستندات بسهولة.
type: docs
weight: 1030
url: /ar/net/aspose.words.drawing.charts/chartlegendentrycollection/
---
## ChartLegendEntryCollection class

يمثل مجموعة من إدخالات أسطورة الرسم البياني.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class ChartLegendEntryCollection : IEnumerable<ChartLegendEntry>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartlegendentrycollection/count/) { get; } | إرجاع عدد[`ChartLegendEntry`](../chartlegendentry/) في هذه المجموعة. |
| [Item](../../aspose.words.drawing.charts/chartlegendentrycollection/item/) { get; } | إرجاع[`ChartLegendEntry`](../chartlegendentry/) للمؤشر المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartlegendentrycollection/getenumerator/)() | يعيد كائن المعداد. |

## أمثلة

يوضح كيفية العمل مع إدخال الأسطورة لسلسلة الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "AW Category 1", "AW Category 2" };

ChartSeries series1 = series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });
series.Add("Series 3", categories, new double[] { 5, 6 });
series.Add("Series 4", categories, new double[] { 0, 0 });

ChartLegendEntryCollection legendEntries = chart.Legend.LegendEntries;
legendEntries[3].IsHidden = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### أنظر أيضا

* class [ChartLegendEntry](../chartlegendentry/)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
