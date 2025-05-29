---
title: ChartFormat.IsDefined
linktitle: IsDefined
articleTitle: IsDefined
second_title: .NET için Aspose.Words
description: Bir formatın ChartFormat IsDefined özelliğiyle tanımlanıp tanımlanmadığını keşfedin. Grafikleriniz için kusursuz biçimlendirme denetiminin kilidini bugün açın!
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.charts/chartformat/isdefined/
---
## ChartFormat.IsDefined property

Herhangi bir formatın tanımlanıp tanımlanmadığını belirten bir bayrak alır.

```csharp
public bool IsDefined { get; }
```

## Örnekler

Seride tanımlanan varsayılan değere dolumun nasıl sıfırlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPoint dataPoint = series.DataPoints[1];

Assert.IsTrue(dataPoint.Format.IsDefined);

dataPoint.Format.SetDefaultFill();

doc.Save(ArtifactsDir + "Charts.ResetDataPointFill.docx");
```

### Ayrıca bakınız

* class [ChartFormat](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
