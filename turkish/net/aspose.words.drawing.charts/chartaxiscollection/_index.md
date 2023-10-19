---
title: ChartAxisCollection Class
linktitle: ChartAxisCollection
articleTitle: ChartAxisCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartAxisCollection sınıf. Grafik eksenlerinin bir koleksiyonunu temsil eder C#'da.
type: docs
weight: 640
url: /tr/net/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class

Grafik eksenlerinin bir koleksiyonunu temsil eder.

```csharp
public class ChartAxisCollection : IEnumerable<ChartAxis>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartaxiscollection/count/) { get; } | Bu koleksiyondaki eksen sayısını alır. |
| [Item](../../aspose.words.drawing.charts/chartaxiscollection/item/) { get; } | Belirtilen dizindeki ekseni alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartaxiscollection/getenumerator/)() | Bir numaralandırıcı nesnesini döndürür. |

## Örnekler

Eksen koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;            

// Birincil ve ikincil Y eksenlerindeki ana ızgara çizgilerini gizleyin.
foreach (ChartAxis axis in chart.Axes)
{
    if (axis.Type == ChartAxisType.Value)
        axis.HasMajorGridlines = false;
}

doc.Save(ArtifactsDir + "Charts.AxisCollection.docx");
```

### Ayrıca bakınız

* class [ChartAxis](../chartaxis/)
* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
