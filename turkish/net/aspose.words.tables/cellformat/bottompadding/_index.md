---
title: CellFormat.BottomPadding
second_title: Aspose.Words for .NET API Referansı
description: CellFormat mülk. Hücre içeriğinin altına eklenecek alan miktarını nokta cinsinden döndürür veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.tables/cellformat/bottompadding/
---
## CellFormat.BottomPadding property

Hücre içeriğinin altına eklenecek alan miktarını (nokta cinsinden) döndürür veya ayarlar.

```csharp
public double BottomPadding { get; set; }
```

### Örnekler

Belge oluşturucuyla hücrelerin nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// İkinci bir hücre ekleyin ve ardından hücre metni dolgu seçeneklerini yapılandırın.
// Oluşturucu bu ayarları mevcut hücresine uygulayacak ve daha sonra oluşturulacak yeni hücrelere uygulayacaktır.
builder.InsertCell();

CellFormat cellFormat = builder.CellFormat;
cellFormat.Width = 250;
cellFormat.LeftPadding = 30;
cellFormat.RightPadding = 30;
cellFormat.TopPadding = 30;
cellFormat.BottomPadding = 30;

builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.EndTable();

// İlk hücre dolgunun yeniden yapılandırılmasından etkilenmedi ve hala varsayılan değerleri koruyor.
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.Width);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.LeftPadding);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.RightPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.TopPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.BottomPadding);

Assert.AreEqual(250.0d, table.FirstRow.Cells[1].CellFormat.Width);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.LeftPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.RightPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.TopPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.BottomPadding);

// İlk hücre, çıktı belgesinde komşu hücrenin boyutuna uyacak şekilde büyümeye devam edecek.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

### Ayrıca bakınız

* class [CellFormat](../)
* ad alanı [Aspose.Words.Tables](../../cellformat/)
* toplantı [Aspose.Words](../../../)


