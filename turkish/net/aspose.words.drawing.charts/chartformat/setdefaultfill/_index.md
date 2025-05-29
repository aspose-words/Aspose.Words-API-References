---
title: ChartFormat.SetDefaultFill
linktitle: SetDefaultFill
articleTitle: SetDefaultFill
second_title: .NET için Aspose.Words
description: Grafik öğenizin dolgusunu orijinal varsayılan değerine zahmetsizce geri yüklemek için ChartFormat SetDefaultFill yöntemini nasıl kullanacağınızı keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing.charts/chartformat/setdefaultfill/
---
## ChartFormat.SetDefaultFill method

Grafik öğesinin dolgusunu varsayılan değere sahip olacak şekilde sıfırlar.

```csharp
public void SetDefaultFill()
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
