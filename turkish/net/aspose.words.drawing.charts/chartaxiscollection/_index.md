---
title: ChartAxisCollection Class
linktitle: ChartAxisCollection
articleTitle: ChartAxisCollection
second_title: .NET için Aspose.Words
description: Grafik eksenlerini verimli bir şekilde yönetmek ve belgenizin veri görselleştirmesini geliştirmek için başvuracağınız çözüm olan Aspose.Words.ChartAxisCollection sınıfını keşfedin.
type: docs
weight: 900
url: /tr/net/aspose.words.drawing.charts/chartaxiscollection/
---
## ChartAxisCollection class

Bir grafik eksenleri koleksiyonunu temsil eder.

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
| [GetEnumerator](../../aspose.words.drawing.charts/chartaxiscollection/getenumerator/)() | Bir numaralandırıcı nesnesi döndürür. |

## Örnekler

Eksen koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Birincil ve ikincil Y eksenlerindeki ana ızgara çizgilerini gizle.
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
