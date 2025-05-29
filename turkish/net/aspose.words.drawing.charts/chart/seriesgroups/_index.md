---
title: Chart.SeriesGroups
linktitle: SeriesGroups
articleTitle: SeriesGroups
second_title: .NET için Aspose.Words
description: Veri görselleştirme deneyiminizi geliştirerek zengin seri grupları koleksiyonuna kolayca erişmek için Chart SeriesGroups özelliğini keşfedin.
type: docs
weight: 90
url: /tr/net/aspose.words.drawing.charts/chart/seriesgroups/
---
## Chart.SeriesGroups property

Bu grafiğin bir seri grubu koleksiyonuna erişim sağlar.

```csharp
public ChartSeriesGroupCollection SeriesGroups { get; }
```

## Örnekler

Boşluk genişliğinin ve örtüşmenin nasıl yapılandırılacağını gösterin.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Sütun boşluk genişliğini ve örtüşmesini ayarlayın.
seriesGroup.GapWidth = 450;
seriesGroup.Overlap = -75;

doc.Save(ArtifactsDir + "Charts.ConfigureGapOverlap.docx");
```

### Ayrıca bakınız

* class [ChartSeriesGroupCollection](../../chartseriesgroupcollection/)
* class [Chart](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
