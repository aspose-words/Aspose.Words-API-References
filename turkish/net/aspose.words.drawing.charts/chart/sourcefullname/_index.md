---
title: Chart.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: .NET için Aspose.Words
description: Gelişmiş veri görselleştirmesi için bağlantılı XLS/XLSX dosyalarının yoluna ve adına kolayca erişmek üzere Chart SourceFullName özelliğini keşfedin.
type: docs
weight: 100
url: /tr/net/aspose.words.drawing.charts/chart/sourcefullname/
---
## Chart.SourceFullName property

Bu grafiğin bağlı olduğu xls/xlsx dosyasının yolunu ve adını alır.

```csharp
public string SourceFullName { get; set; }
```

## Örnekler

Grafik bağlantılıysa harici xls/xlsx belgesinin tam adının nasıl alınacağını/ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

var sourceFullName = shape.Chart.SourceFullName;
Assert.True(sourceFullName.Contains("Examples\\Data\\Spreadsheet.xlsx"));
```

### Ayrıca bakınız

* class [Chart](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
