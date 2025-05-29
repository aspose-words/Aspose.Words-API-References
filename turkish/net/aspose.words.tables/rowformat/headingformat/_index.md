---
title: RowFormat.HeadingFormat
linktitle: HeadingFormat
articleTitle: HeadingFormat
second_title: .NET için Aspose.Words
description: RowFormat HeadingFormat özelliğini keşfedin, çok sayfalı belgelerde açıklık ve okunabilirliği artırmak için tablo başlıklarınızın her sayfada tekrarlandığından emin olun.
type: docs
weight: 30
url: /tr/net/aspose.words.tables/rowformat/headingformat/
---
## RowFormat.HeadingFormat property

Tablo birden fazla sayfaya yayıldığında satır her sayfada tablo başlığı olarak tekrarlanıyorsa doğrudur.

```csharp
public bool HeadingFormat { get; set; }
```

## Örnekler

Her sayfada tekrarlanan satırlardan oluşan bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// "HeadingFormat" bayrağı "true" olarak ayarlandığında eklenen tüm satırlar
// yayıldığı her sayfada tablonun en üstünde görünecektir.
builder.RowFormat.HeadingFormat = true;
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.CellFormat.Width = 100;
builder.InsertCell();
builder.Write("Heading row 1");
builder.EndRow();
builder.InsertCell();
builder.Write("Heading row 2");
builder.EndRow();

builder.CellFormat.Width = 50;
builder.ParagraphFormat.ClearFormatting();
builder.RowFormat.HeadingFormat = false;

// Tablonun iki sayfaya yayılması için yeterli sayıda satır ekleyin.
for (int i = 0; i < 50; i++)
{
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 1.");
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 2.");
    builder.EndRow();
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableSetHeadingRow.docx");
```

### Ayrıca bakınız

* class [RowFormat](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
