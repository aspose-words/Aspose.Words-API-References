---
title: CellFormat.BottomPadding
linktitle: BottomPadding
articleTitle: BottomPadding
second_title: .NET için Aspose.Words
description: Hücrelerinizdeki aralıkları özelleştirmek için CellFormat BottomPadding özelliğini keşfedin. Daha iyi sunum için düzenlerinizi hassas nokta ayarlamalarıyla geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.tables/cellformat/bottompadding/
---
## CellFormat.BottomPadding property

Hücrenin içeriğinin altına eklenecek boşluk miktarını (nokta cinsinden) döndürür veya ayarlar.

```csharp
public double BottomPadding { get; set; }
```

## Örnekler

Belge oluşturucuyla hücrelerin nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// İkinci bir hücre ekleyin ve ardından hücre metin dolgusu seçeneklerini yapılandırın.
// Oluşturucu bu ayarları mevcut hücreye uygulayacak ve daha sonra oluşturulan tüm yeni hücrelere uygulayacaktır.
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

// İlk hücre, dolgu yeniden yapılandırmasından etkilenmedi ve hala varsayılan değerleri koruyor.
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

// İlk hücre, komşu hücresinin boyutuna uyacak şekilde çıktı belgesinde büyümeye devam edecektir.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

### Ayrıca bakınız

* class [CellFormat](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
