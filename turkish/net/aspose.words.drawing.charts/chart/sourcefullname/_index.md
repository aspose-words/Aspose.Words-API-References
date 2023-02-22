---
title: Chart.SourceFullName
second_title: Aspose.Words for .NET API Referansı
description: Chart mülk. Bu grafiğin bağlantılı olduğu bir xls/xlsx dosyasının yolunu ve adını alır.
type: docs
weight: 60
url: /tr/net/aspose.words.drawing.charts/chart/sourcefullname/
---
## Chart.SourceFullName property

Bu grafiğin bağlantılı olduğu bir xls/xlsx dosyasının yolunu ve adını alır.

```csharp
public string SourceFullName { get; set; }
```

### Örnekler

Grafik bağlantılıysa, harici xls/xlsx belgesinin tam adının nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Shape with linked chart.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.True(shape.Chart.SourceFullName.Contains("Examples\\Data\\Spreadsheet.xlsx"));
```

### Ayrıca bakınız

* class [Chart](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chart/)
* toplantı [Aspose.Words](../../../)


