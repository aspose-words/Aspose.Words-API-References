---
title: Chart.SourceFullName
second_title: Aspose.Words for .NET API Referansı
description: Chart mülk. Bu grafiğin bağlı olduğu xls/xlsx dosyasının yolunu ve adını alır.
type: docs
weight: 70
url: /tr/net/aspose.words.drawing.charts/chart/sourcefullname/
---
## Chart.SourceFullName property

Bu grafiğin bağlı olduğu xls/xlsx dosyasının yolunu ve adını alır.

```csharp
public string SourceFullName { get; set; }
```

### Örnekler

Grafik bağlıysa harici xls/xlsx belgesinin tam adının nasıl alınacağını/ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

var sourceFullName = shape.Chart.SourceFullName;
Assert.True(sourceFullName.Contains("Examples\\Data\\Spreadsheet.xlsx"));

sourceFullName = "D:\\Documents\\ChartData.xlsx";
Assert.True(sourceFullName.Equals("D:\\Documents\\ChartData.xlsx", StringComparison.Ordinal));
```

### Ayrıca bakınız

* class [Chart](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chart/)
* toplantı [Aspose.Words](../../../)


